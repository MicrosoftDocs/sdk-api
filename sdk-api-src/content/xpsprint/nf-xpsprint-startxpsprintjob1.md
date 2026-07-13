---
UID: NF:xpsprint.StartXpsPrintJob1
title: StartXpsPrintJob1 function (xpsprint.h)
description: Creates a print job for sending XPS document content to a printer.
helpviewer_keywords: ["StartXpsPrintJob1","StartXpsPrintJob1 function [Windows GDI]","gdi.startxpsprintjob1","xpsprint/StartXpsPrintJob1"]
old-location: gdi\startxpsprintjob1.htm
tech.root: xps
ms.assetid: 91D0BA4D-60A6-43F8-8BD3-9183DC6CD50D
ms.date: 12/05/2018
ms.keywords: StartXpsPrintJob1, StartXpsPrintJob1 function [Windows GDI], gdi.startxpsprintjob1, xpsprint/StartXpsPrintJob1
req.header: xpsprint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 with SP1, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 with SP1, Windows Server 2008 and Platform Update Supplement for Windows Server 2008 [desktop apps only]
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
 - StartXpsPrintJob1
 - xpsprint/StartXpsPrintJob1
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
 - StartXpsPrintJob1
---

# StartXpsPrintJob1 function


## -description

<p class="CCE_Message">[StartXpsPrintJob1 is not supported and may be altered or unavailable in the future. ]

Creates a print job for sending XPS document content to a printer.This function creates a more efficient print path than <a href="/windows/desktop/api/xpsprint/nf-xpsprint-startxpsprintjob">StartXpsPrintJob</a>.

## -parameters

### -param printerName [in]

The name of the printer with which this job will be associated.

### -param jobName [in, optional]

A user-specified  job name to be associated with this job.  You can set this parameter to <b>NULL</b> if the job does not require a  separate, user-specified name.

### -param outputFileName [in, optional]

The  file name of the file or port into which the output of this job is to be redirected.  Setting this value will cause the output of the print job to be directed to the specified file or port. To send the print job to the printer that is specified by <i>printerName</i>, you must set this parameter to <b>NULL</b>.

### -param progressEvent [in, optional]

An event handle that is signaled when one of the following print job changes occur:
<ul>
<li>A job ID is assigned to the print job</li>
<li>Printing of a page has finished</li>
<li>Printing of a document has finished</li>
<li>The print job has been canceled or has ended because of an error</li>
</ul>



<div class="alert"><b>Note</b>  This event will not be signaled until after the application has started sending data to the print job.</div>
<div> </div>


The XPS Print API does not reset this event—that is the caller's responsibility.


Set this parameter to <b>NULL</b> if you do not want to be notified about  progress.

### -param completionEvent [in, optional]

An event handle that is signaled when the  print job finishes.  This event is guaranteed to be signaled exactly once per <b>StartXpsPrintJob1</b> call.  The XPS Print API does not reset this event—that is the caller's responsibility.

Set this parameter to <b>NULL</b> if do not want to be notified about completion.

### -param xpsPrintJob [out, optional]

A pointer to the <a href="/windows/desktop/api/xpsprint/nn-xpsprint-ixpsprintjob">IXpsPrintJob</a> interface that represents the print job that  <b>StartXpsPrintJob1</b> created.  To get the status of the print job or to cancel it, use the <b>IXpsPrintJob</b> interface. Set this parameter to <b>NULL</b> if you do not need it.

### -param printContentReceiver [out]

A pointer to the <a href="/previous-versions/windows/desktop/ff970304(v=vs.85)">IXpsOMPackageTarget</a> interface that this function created. This parameter is required and you cannot set it to <b>NULL</b>.

To send document content to the print job that this function created, use the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a> interface that you  create by calling the <a href="/previous-versions/windows/desktop/ff970305(v=vs.85)">CreateXpsOMPackageWriter</a> method of the <a href="/previous-versions/windows/desktop/ff970304(v=vs.85)">IXpsOMPackageTarget</a> interface returned in <i>xpsOMPackageTarget</i>.

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
<i>printerName</i> or <i>xpsOMPackageTarget</i> is <b>NULL</b>.

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

<b>StartXpsPrintJob1</b> is an asynchronous function, and therefore it can return before the print spooler creates or starts a print job.

Do not use the interfaces that are returned in <i>xpsPrintJob</i> and <i>xpsOMPackageTarget</i> until <b>StartXpsPrintJob1</b> has returned successfully.

  After the caller starts sending data, it is a good programming practice to monitor the progress events that are signaled to the event that is passed in <i>progressEvent</i>. When the event is signaled, the caller must  call <a href="/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjob-getjobstatus">IXpsPrintJob::GetJobStatus</a> to get the current status of the print job.

When the print job finishes, whether successfully or not, the event that is passed in <i>completionEvent</i> is signaled only once. To prevent data loss, it is a good programming practice for the caller to monitor the completion event and ensure that neither the thread nor the application that created the print job are terminated until the completion event  has been signaled.

Job states are neither stored nor queued by the print spooler. Because job processing does not wait for the status to be read after events are signaled,  the caller might miss some state changes, depending on the delay between the time the application received the change notification and the time it called <a href="/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjob-getjobstatus">IXpsPrintJob::GetJobStatus</a>. To receive subsequent notifications, the application must reset the progress event after it has received the notification.

If a call to <b>StartXpsPrintJob1</b> fails,  the print spooler updates the job status, signals the  completion and progress events, and returns an error code. To get the status of the failed print job, call <a href="/windows/desktop/api/xpsprint/nf-xpsprint-ixpsprintjob-getjobstatus">IXpsPrintJob::GetJobStatus</a>.

<b>StartXpsPrintJob1</b> calls <b>DuplicateHandle</b> on <i>completionEvent</i> and <i>progressEvent</i> to ensure that they remain valid for the lifetime of the job.  Because the print spooler is using a duplicate handle for the events,   the caller can close these handles at any point without affecting job execution.  However,  we recommend for the caller to close these handles only after the <i>completionEvent</i> event has been signaled and the caller observed it.

<div class="alert"><b>Note</b>   When your application prints to a file, the application is responsible for providing the value to pass in the <i>outputFileName</i> parameter for print-to-file operations.  To print to a printer that uses a  driver that outputs to the FILE: port, the caller must retrieve the file name from the user by displaying the common file dialog box.
</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/dd316975(v=vs.85)">Documents</a>



<a href="/previous-versions/windows/desktop/ff970304(v=vs.85)">IXpsOMPackageTarget</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter">IXpsOMPackageWriter</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>