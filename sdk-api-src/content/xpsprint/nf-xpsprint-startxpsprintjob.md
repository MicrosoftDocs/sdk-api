---
UID: NF:xpsprint.StartXpsPrintJob
title: StartXpsPrintJob function (xpsprint.h)
description: Starts printing an XPS document stream to a printer.
helpviewer_keywords: ["StartXpsPrintJob","StartXpsPrintJob function [Windows GDI]","gdi.startxpsprintjob","xpsprint/StartXpsPrintJob"]
old-location: gdi\startxpsprintjob.htm
tech.root: xps
ms.assetid: d982ae2e-c68f-4197-b419-22a63e61db8a
ms.date: 12/05/2018
ms.keywords: StartXpsPrintJob, StartXpsPrintJob function [Windows GDI], gdi.startxpsprintjob, xpsprint/StartXpsPrintJob
req.header: xpsprint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: XpsPrint.lib
req.dll: XpsPrint.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StartXpsPrintJob
 - xpsprint/StartXpsPrintJob
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - XpsPrint.dll
api_name:
 - StartXpsPrintJob
---

# StartXpsPrintJob function


## -description

<p class="CCE_Message">[StartXpsPrintJob is not supported and may be altered or unavailable in the future. ]

Starts printing an XPS document stream to a printer.

## -parameters

### -param printerName [in]

The name of the printer with which this job will be associated.

### -param jobName [in]

A user-specified  job name to be associated with this job.  If the job does not require a  separate, user-specified name, this parameter can be set to <b>NULL</b>.

### -param outputFileName [in]

The  file name of the file or port into which the output of this job is to be redirected.  Setting this value will cause the output of the print job to be directed to the specified file or port. To send the print job to the printer that is specified by <i>printerName</i>, this parameter must be set to <b>NULL</b>.

### -param progressEvent [in]

An event handle that is signaled when the following print job changes occur:
<ul>
<li>A job ID is assigned to the print job</li>
<li>Printing of a page has finished</li>
<li>Printing of a document has finished</li>
<li>The print job has been canceled or has ended because of an error</li>
</ul>



<div class="alert"><b>Note</b>  This event will not be signaled until after the application has started sending data to the print job.</div>
<div> </div>


The XPS Print API does not reset this event—that is the caller's responsibility.


If no progress notification is required, this parameter can be set to <b>NULL</b>.

### -param completionEvent [in]

An event handle that is signaled when the  print job finishes.  This event is guaranteed to be signaled exactly once per <b>StartXpsPrintJob</b> call.  The XPS Print API does not reset this event—that is the caller's responsibility.

If no completion notification is required, this parameter can be set to <b>NULL</b>.

### -param printablePagesOn [in]

The parameter references a UINT8 array whose elements specify a subset of a document's pages to be printed. As shown in the table that follows, the value of each element indicates whether the page is to be printed.

<table>
<tr>
<th>Array Element Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Do not print the page.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>Non-zero</dt>
</dl>
</td>
<td width="60%">
Print the page.

</td>
</tr>
</table>
 

Progress events will  be signaled only for the pages that are designated for printing.  

The elements in the array represent all pages that are designated for printing, in all  documents of the XPS package.  For example, if the package contains two documents that have three pages each, the array shown in the following table designates the printing of pages 0 and 2 from document 1, and pages 0 and 2 from document 2.  

<table>
<tr>
<th>Element index</th>
<th>Element Value</th>
<th>Print?</th>
<th>Document number</th>
<th>Page number</th>
</tr>
<tr>
<td>5</td>
<td>1</td>
<td>Yes</td>
<td>2</td>
<td>2</td>
</tr>
<tr>
<td>4</td>
<td>0</td>
<td>No</td>
<td>2</td>
<td>1</td>
</tr>
<tr>
<td>3</td>
<td>1</td>
<td>Yes</td>
<td>2</td>
<td>0</td>
</tr>
<tr>
<td>2</td>
<td>1</td>
<td>Yes</td>
<td>1</td>
<td>2</td>
</tr>
<tr>
<td>1</td>
<td>0</td>
<td>No</td>
<td>1</td>
<td>1</td>
</tr>
<tr>
<td>0</td>
<td>1</td>
<td>Yes</td>
<td>1</td>
<td>0</td>
</tr>
</table>
 

If <i>printablePagesOn</i> is <b>NULL</b>, all pages in the package will be printed.

If <i>printablePagesOn</i> has more elements than there are pages in the package, the superfluous elements will be ignored.

If the array has fewer elements than there are pages in the document, the value of the last array element of the array is applied to the remaining pages.  This rule makes it easier to specify a range that is open-ended or that gets only a few pages of a large  document printed.

### -param printablePagesOnCount [in]

The number of elements in the array that is referenced by <i>printablePagesOn</i>.  If <i>printablePagesOn</i> is <b>NULL</b>, this parameter is ignored.

### -param xpsPrintJob [out]

A pointer to the <a href="/windows/desktop/api/xpsprint/nn-xpsprint-ixpsprintjob">IXpsPrintJob</a> interface that represents the print job that is created by <b>StartXpsPrintJob</b>.  To get the status of the print job or to cancel it, use the <b>IXpsPrintJob</b> interface. If an <b>IXpsPrintJob</b> is not required, this parameter can be set to <b>NULL</b>.

### -param documentStream [out]

A pointer to the <a href="/windows/desktop/api/xpsprint/nn-xpsprint-ixpsprintjobstream">IXpsPrintJobStream</a> interface into which the caller  writes the XPS document to be printed by this print job.

### -param printTicketStream [out]

A pointer to the <a href="/windows/desktop/api/xpsprint/nn-xpsprint-ixpsprintjobstream">IXpsPrintJobStream</a> interface that is  used by  the caller to write the job-level print ticket that will be associated with this job.  If this parameter is set to <b>NULL</b>, the print tickets (if any exist) from the XPS document that is written to <i>documentStream</i> will be used.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>printerName</i> or <i>documentStream</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory to create a new <a href="/windows/desktop/api/xpsprint/nn-xpsprint-ixpsprintjob">IXpsPrintJob</a> object.


</td>
</tr>
</table>

## -remarks

<b>StartXpsPrintJob</b> is an asynchronous function, which can return before the print spooler creates or starts a print job.

The interfaces that are returned in <i>xpsPrintJob</i>, <i>documentStream</i>, and <i>printTicketStream</i> must not be used until <b>StartXpsPrintJob</b> has returned successfully.

  After the caller starts sending data, it should monitor the progress events that are signaled to the event that is passed in <i>progressEvent</i>. When the event is signaled, the caller must  call <a href="/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjob-getjobstatus">IXpsPrintJob::GetJobStatus</a> to get the current status of the print job.

When the print job finishes, whether successfully or not, the event that is passed in <i>completionEvent</i> is signaled once and only once. To prevent data loss, the caller should monitor this event and the thread or the application of the caller should not be terminated until the event  has been signaled.

Job states are neither stored nor queued by the print spooler. Because job processing does not wait for the status to be read after events are signaled,  the caller might miss some state changes, depending on the delay between the time the application received the change notification and the time it called <a href="/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjob-getjobstatus">IXpsPrintJob::GetJobStatus</a>. To receive subsequent notifications, the application must reset the progress event after it has received the notification.

If a call to <b>StartXpsPrintJob</b> fails,  the job status will be updated, the  completion and progress events will be signaled, and an error code will be returned. To get the status of the failed print job, call <a href="/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjob-getjobstatus">IXpsPrintJob::GetJobStatus</a>.

<b>StartXpsPrintJob</b> calls <b>DuplicateHandle</b> on <i>completionEvent</i> and <i>progressEvent</i> to ensure that they remain valid for the lifetime of the job.  Because the print spooler is using a duplicate handle for the events,  it is possible for the caller to close these handles at any point without affecting job execution.  The recommended procedure, however,  is for the caller to close these handles only after the <i>completionEvent</i> event has been signaled and observed by the caller.

The <a href="/windows/desktop/api/xpsprint/nn-xpsprint-ixpsprintjobstream">IXpsPrintJobStream</a> interfaces that are returned in <i>documentStream</i>  and <i>printTicketStream</i> are write-only streams that do not permit seeking but that can be closed. The caller writes the  XPS document and print ticket content into these streams, and then calls <a href="/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjobstream-close">Close</a> after all data has been written.  Calls to the streams' <b>Write</b>   method    are thread-safe; however, if such calls  are made from different threads, they are not guaranteed to be committed to the stream in the expected order.

<div class="alert"><b>Note</b>   When printing to a file, the application is responsible for providing the value that will be passed in the <i>outputFileName</i> parameter for print-to-file operations.  To print to a printer which uses a  driver that outputs to the FILE: port, the caller must retrieve the file name from the user by displaying the common file dialog.
</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/dd316975(v=vs.85)">Documents</a>



<a href="/windows/desktop/api/xpsprint/nf-xpsprint-startxpsprintjob1">StartXpsPrintJob1</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>