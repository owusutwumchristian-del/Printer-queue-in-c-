#include <iostream>
#include <queue>
#include <string>
using namespace std;

class PrintJob {
public:
    string document;
    PrintJob(string doc) : document(doc) {}
};

int main() {
    queue<PrintJob> printerQueue;

    // Enqueue print jobs
    printerQueue.push(PrintJob("Assignment.pdf"));
    printerQueue.push(PrintJob("LectureNotes.docx"));
    printerQueue.push(PrintJob("ProjectReport.pptx"));

    // Process jobs
    while (!printerQueue.empty()) {
        PrintJob job = printerQueue.front();
        cout << "Printing: " << job.document << endl;
        printerQueue.pop();
    }

    return 0;
}
