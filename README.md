function calculateMarks(students) {
    students.forEach(student => {
        
        let totalMarks = Object.values(student.marks).reduce((acc, mark) => acc + mark, 0);
       
        let averageMarks = totalMarks / Object.keys(student.marks).length;

        
        let hasPassed = averageMarks >= 50; 
       
        console.log(`Student: ${student.name}`);
        console.log(`Total Marks: ${totalMarks}`);
        console.log(`Average Marks: ${averageMarks.toFixed(2)}`);
        console.log(`Passed: ${hasPassed ? "Yes" : "No"}`);
        console.log('-------------------------');
    });
}


let studentsArray = [
    {
        name: "Alice",
        marks: {
            math: 85,
            science: 90,
            english: 88
        }
    },
    {
        name: "Bob",
        marks: {
            math: 45,
            science: 60,
            english: 55
        }
    },
    {
        name: "Charlie",
        marks: {
            math: 70,
            science: 80,
            english: 75
        }
    }
];

calculateMarks(studentsArray);
