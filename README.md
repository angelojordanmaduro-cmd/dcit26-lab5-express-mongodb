Open your project terminal in VS Code and run: npm install

Create a .env file in the root directory (you can copy .env.example) and add your configuration: PORT=5000

MONGODB_URI=your_mongodb_connection_string
Run the development server using nodemon: npm run dev

Navigate to http://localhost:5000/api/health.
You should see: {
  "success": true,
  "message": "Student Records API is running"
}
Health Check: curl.exe http://localhost:5000/api/health
Get All Students: curl.exe http://localhost:5000/api/students
Create a Student (POST): curl.exe -X POST http://localhost:5000/api/students -H "Content-Type: application/json" -d "{\"fullName\":\"Alex Santos\",\"course\":\"BSIT\",\"yearLevel\":2,\"section\":\"IT-2A\"}"
Update Student (PUT): curl.exe -X PUT http://localhost:5000/api/students/<STUDENT_ID> -H "Content-Type: application/json" -d "{\"fullName\":\"Alex Santos\",\"course\":\"BSIT\",\"yearLevel\":3,\"section\":\"IT-3A\"}"
Delete Student (DELETE): curl.exe -X DELETE http://localhost:5000/api/students/<STUDENT_ID>
