This is where the source code starts.


In general, this is a three-tier architecture even for the Desktop version. The source code can be divided into three parts:

* Database manipulation logics including CRUD operations. For the desktop version, it is planned to use SQLite. The problem is that it does not support SQL-level UDF definition with “CREATE FUNCTION”. C-level extensions are required, which adds additional complexities in the whole system. One solution is to weak the concept of in-database analysis by moving this kinds of logics from DB into the application logics, i.e. in NodeJS code base.

* The application code implemented in NodeJS frameworks using server-side JavaScript. This part will be a combination of JS and TypeScript. Interfaces with the database and the frontend will be the major challenge.

* Frontend logics. For the Desktop version, the frontend with be based on the Electron framework. The implementation language will be mainly JavaScript or TypeScript. The design rationale is to use as much as possible Web technologies (HTML5) to provide the class-leading user experience. This will be the used as the basis for the future version in the Web and in the Cloud. 
