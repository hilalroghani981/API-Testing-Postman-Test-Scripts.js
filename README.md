
// API Testing - Postman Assertions
// Tester: Hilal Roghani

pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Name is Hilal", function () {
    const response = pm.response.json();
    pm.expect(response.json.name).to.eql("Hilal");
});

pm.test("Course is correct", function () {
    const response = pm.response.json();
    pm.expect(response.json.course).to.eql("Manual QA Testing");
});
