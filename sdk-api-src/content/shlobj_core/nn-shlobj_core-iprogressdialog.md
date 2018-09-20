---
UID: NN:shlobj_core.IProgressDialog
title: IProgressDialog
author: windows-sdk-content
description: Exposes methods that provide options for an application to display a progress dialog box.
old-location: shell\IProgressDialog.htm
tech.root: shell
ms.assetid: ba0fb1f9-f67f-4cc7-96d8-4c4ccdd213eb
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IProgressDialog, IProgressDialog interface [Windows Shell], IProgressDialog interface [Windows Shell],described, _win32_IProgressDialog, shell.IProgressDialog, shlobj_core/IProgressDialog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IProgressDialog
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IProgressDialog interface


## -description


Exposes methods that provide options for an application to display a progress dialog box. This interface is exported by the progress dialog box object (CLSID_ProgressDialog). This object is a generic way to show a user how an operation is progressing. It is typically used when deleting, uploading, copying, moving, or downloading large numbers of files.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IProgressDialog</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IProgressDialog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IProgressDialog</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd817850-7776-47cd-b1b3-ccb946660781">HasUserCancelled</a>
</td>
<td align="left" width="63%">
Checks whether the user has canceled the operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc974be9-e9a4-42f9-9995-0d6eb0b12422">SetAnimation</a>
</td>
<td align="left" width="63%">
Specifies an AVI clip that runs in the dialog box.
        
            

<div class="alert"><b>Note</b>  This method is not supported in Windows Vista or later versions.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/520e11c0-f356-45e1-a300-cc14e88eb42e">SetCancelMsg</a>
</td>
<td align="left" width="63%">
Sets a message to be displayed if the user cancels the operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2c4441a8-3bb6-4cd8-8f96-423ee8d26113">SetLine</a>
</td>
<td align="left" width="63%">
Displays a message in the progress dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50df7b32-e345-4379-809f-6870b53417b8">SetProgress</a>
</td>
<td align="left" width="63%">
Updates the progress dialog box with the current state of the operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/829775a0-5dd0-4c5e-8b92-b34c7d75f15e">SetProgress64</a>
</td>
<td align="left" width="63%">
Updates the progress dialog box with the current state of the operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5474ab2-bd13-45ba-9df5-977b909b0726">SetTitle</a>
</td>
<td align="left" width="63%">
Sets the title of the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0cafe878-c95f-416e-8291-51d9a5a17a71">StartProgressDialog</a>
</td>
<td align="left" width="63%">
Starts the progress dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a46ca72-b19d-4fd3-b783-2d182326deb4">StopProgressDialog</a>
</td>
<td align="left" width="63%">
Stops the progress dialog box and removes it from the screen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab048787-e555-4d5d-994a-1fc6f273312b">Timer</a>
</td>
<td align="left" width="63%">
Resets the progress dialog box timer to zero.

</td>
</tr>
</table> 


## -remarks



The progress dialog box object creates a modeless dialog box and allows the client to set its title, animation, text lines, and progress bar. The object then handles updating on a background thread and allows the user to cancel the operation. Optionally, it estimates the time remaining until the operation is complete and displays the information as a line of text.

Applications normally do not implement this interface. It is exported by the progress dialog box object for use by applications.

Use this interface when your application needs to display a progress dialog box. To initialize the object:

				

<ol>
<li>Create an in-process progress dialog box object (CLSID_ProgressDialog) with <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>. Request a 
pointer to its <b>IProgressDialog</b> interface (IID_IProgressDialog).</li>
<li>Call <a href="https://msdn.microsoft.com/c5474ab2-bd13-45ba-9df5-977b909b0726">IProgressDialog::SetTitle</a> to specify the dialog box title.</li>
<li>Call <a href="https://msdn.microsoft.com/cc974be9-e9a4-42f9-9995-0d6eb0b12422">IProgressDialog::SetAnimation</a> to specify an AVI clip to be played while the operation progresses.</li>
<li>Call <a href="https://msdn.microsoft.com/520e11c0-f356-45e1-a300-cc14e88eb42e">IProgressDialog::SetCancelMsg</a> to specify the message that will be displayed if the user cancels the operation.</li>
</ol>
To display the progress of the operation:
				

<ol>
<li>Call <a href="https://msdn.microsoft.com/0cafe878-c95f-416e-8291-51d9a5a17a71">IProgressDialog::StartProgressDialog</a> to display the dialog box.</li>
<li>Assign a numerical value to the total amount of work the operation will perform. Use any number that allows you to conveniently define the progress of the operation. For example, set this value to 100 if you want to specify the progress of the operation in terms of the percent that has been completed.</li>
<li>Call <a href="https://msdn.microsoft.com/ab048787-e555-4d5d-994a-1fc6f273312b">IProgressDialog::Timer</a> to reset the timer. This method sets the starting point that the progress dialog object uses to estimate the time remaining in the operation. If you do not call this method, the starting point will be the call to <a href="https://msdn.microsoft.com/0cafe878-c95f-416e-8291-51d9a5a17a71">StartProgressDialog</a>.</li>
<li>As the operation progresses, periodically call <a href="https://msdn.microsoft.com/50df7b32-e345-4379-809f-6870b53417b8">IProgressDialog::SetProgress</a> to update the dialog box as to how much of the operation has been completed. The progress dialog object will update its progress bar and recalculate its estimate of the remaining time. You can use any numerical measure of progress that is convenient. However, if you want to use values larger than 4 gigabytes (GB), you must call <a href="https://msdn.microsoft.com/829775a0-5dd0-4c5e-8b92-b34c7d75f15e">IProgressDialog::SetProgress64</a> instead of <b>IProgressDialog::SetProgress</b>.</li>
<li>Your application does not receive a notification if the user clicks the <b>Cancel</b> button to cancel the operation. As the operation progresses, periodically call <a href="https://msdn.microsoft.com/bd817850-7776-47cd-b1b3-ccb946660781">IProgressDialog::HasUserCancelled</a> to see if the user has clicked the <b>Cancel</b> button. Applications typically call this method each time they call <a href="https://msdn.microsoft.com/50df7b32-e345-4379-809f-6870b53417b8">IProgressDialog::SetProgress</a> or <a href="https://msdn.microsoft.com/829775a0-5dd0-4c5e-8b92-b34c7d75f15e">IProgressDialog::SetProgress64</a>.</li>
<li>The dialog box displays three lines of text. An application can periodically call <a href="https://msdn.microsoft.com/2c4441a8-3bb6-4cd8-8f96-423ee8d26113">IProgressDialog::SetLine</a> to display a message on one of these lines. This method is normally used to provide information on the current status of the operation. A typical message is something like: "Currently processing item XXX...". Messages are typically displayed on lines 1 and 2. You can display messages on line 3 only if you have not instructed the progress dialog object to estimate the remaining time by setting the <b>PROGDLG_AUTOTIME</b> flag in the <i>dwFlags</i> parameter of <a href="https://msdn.microsoft.com/0cafe878-c95f-416e-8291-51d9a5a17a71">IProgressDialog::StartProgressDialog</a>. In that case, the third text line is used to display the estimated time.</li>
</ol>
When the operation is complete:
				

<ol>
<li>Call <a href="https://msdn.microsoft.com/6a46ca72-b19d-4fd3-b783-2d182326deb4">IProgressDialog::StopProgressDialog</a> to close the dialog box.</li>
<li>Release the progress dialog box object.</li>
</ol>


