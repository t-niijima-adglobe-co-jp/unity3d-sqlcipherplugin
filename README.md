# SQLCipherForUnity3D
Plugin to bind SQLite/SQLCipher database to Unity [iOS, Android, MAC , Windows], you can view this tutorial for more detail @ http://dotosoft.com/bind-sqlcipher-in-unity3d/

<b>***** please don't use this code for sell an asset *****</b>

##change log
###v 1.0 :
* Android + IOS Support
* sqlite + sqlcipher libs version for Android
* SQLPlugin.mm to bridge SQLite Unity to IOS
* Add UnityORM that convert Object/UserDefined to SQL, and vice versa



###How to Use:

	SqliteDatabase sqlDB = new SqliteDatabase(“yourdatabasefile”, “yourdirectory”); // init database....
	sqlDB.Open(); // to open database....
	database.Key("yourpassword"); // if you use sqlcipher to encrypt your database file....
	string query = “SQL QUERY”; //your sql query....
	sqlDB.ExecuteNonQuery(query); //execute Update/Insert sql....
	DataTable tableData = sqlDB.ExecuteQuery (query); //execute query sql....
	sqlDB.Close(); // to close database....


####IMPORTANT: 
  If you have created database before, please put at StreamingAssets folder, because the second parameter at SqliteDatabase class is relative path from that folder. If you don't have database, it will create new one at your device persistent path when you deploy at runtime. Please read Unity Manual for more detail.


###to execute a query this libs have 3 simple methods:

	ExecuteNonQuery(string query, object[] param)  //for SQL query like UPDATE, DELETE....
	DataTable ExecuteQuery (string query, object[] param)  //for SQL query like SELECT ....
	void ExecuteScript(string script) // for batch script


# credits
 * First version developed by Poya  @  http://gamesforsoul.com/
 * BLOB support by Jonathan Derrough @ http://jderrough.blogspot.com/
 * modified by Dotosoft Studio @ http://dotosoft.com

<br/>

####feedback?

* twitter: [@dotosoft](http://www.twitter.com/dotosoft)
* mail: <dotosoft@gmail.com>
* <http://dotosoft.com>
