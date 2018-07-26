---
UID: NN:shobjidl_core.IFileDialog
title: IFileDialog
author: windows-sdk-content
description: Exposes methods that initialize, show, and get results from the common file dialog.
old-location: shell\IFileDialog.htm
old-project: shell
ms.assetid: 9341bb68-2410-4e03-8acd-fef29287b61c
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IFileDialog, IFileDialog interface [Windows Shell], IFileDialog interface [Windows Shell],described, shell.IFileDialog, shell_IFileDialog, shobjidl_core/IFileDialog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileDialog
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IFileDialog interface


## -description


Exposes methods that initialize, show, and get results from the common file dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileDialog</b> interface inherits from <a href="https://msdn.microsoft.com/e9d640fd-ef10-486a-a037-01b7a71179a0">IModalWindow</a>. <b>IFileDialog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileDialog</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2196e73f-4e0f-4213-b0a2-13a047486f40">AddPlace</a>
</td>
<td align="left" width="63%">
Adds a folder to the list of places available for the user to open or save items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5664a52-f26c-475d-84ef-0c657ae46e2e">Advise</a>
</td>
<td align="left" width="63%">
Assigns an event handler that listens for events coming from the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bedb6fc8-7db7-4d29-a223-a9997b57c8a3">ClearClientData</a>
</td>
<td align="left" width="63%">
Instructs the dialog to clear all persisted state information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Closes the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3768c15-d933-43c0-8398-f8f1c16ecbf9">GetCurrentSelection</a>
</td>
<td align="left" width="63%">
Gets the user's current selection in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926842">GetFileName</a>
</td>
<td align="left" width="63%">
Retrieves the text currently entered in the dialog's <b>File name</b> edit box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae5b08a1-a97d-433b-88dc-938abe028384">GetFileTypeIndex</a>
</td>
<td align="left" width="63%">
Gets the currently selected file type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/424d1507-e42a-43d7-8904-347bfb311dd4">GetFolder</a>
</td>
<td align="left" width="63%">
Gets either the folder currently selected in the dialog, or, if the dialog is not currently displayed, the folder that is to be selected when the dialog is opened.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451244">GetOptions</a>
</td>
<td align="left" width="63%">
Gets the current flags that are set to control dialog behavior.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6572f172-8b66-4b42-b087-d0133595b380">GetResult</a>
</td>
<td align="left" width="63%">
Gets the choice that the user made in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ab7d8bb-068d-4c5b-b273-68c7fc4f9956">SetClientGuid</a>
</td>
<td align="left" width="63%">
Enables a calling application to associate a GUID with a dialog's persisted state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e1739f4-d229-4bf1-99f4-6bded830de2b">SetDefaultExtension</a>
</td>
<td align="left" width="63%">
Sets the default extension to be added to file names.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dcde0f80-8118-479d-a08c-4b9af6aa343a">SetDefaultFolder</a>
</td>
<td align="left" width="63%">
Sets the folder used as a default if there is not a recently used folder value available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8b72a76-6cdb-4675-8d84-f3c7171b8576">SetFileName</a>
</td>
<td align="left" width="63%">
Sets the file name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4dc456c4-e06a-4bbf-b7c3-a6f93b46a044">SetFileNameLabel</a>
</td>
<td align="left" width="63%">
Sets the text of the label next to the file name edit box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/733ade05-e255-4b1c-a961-e1feb749f73d">SetFileTypeIndex</a>
</td>
<td align="left" width="63%">
Sets the file type that appears as selected in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca850988-7f2f-4faf-9ded-14db476fc452">SetFileTypes</a>
</td>
<td align="left" width="63%">
Sets the file types that the dialog can open or save.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f650ae2-77c4-496c-8b8b-279c69eaaf65">SetFilter</a>
</td>
<td align="left" width="63%">
<b>Deprecated in Windows 7.</b> Sets the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f300c70-cae8-43bb-95d4-25ac4be9b4c4">SetFolder</a>
</td>
<td align="left" width="63%">
Sets a folder that is always selected when the dialog is opened, regardless of previous user action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4320de0f-bfa6-4e17-a09d-d004559fae70">SetOkButtonLabel</a>
</td>
<td align="left" width="63%">
Sets the text of the <b>Open</b> or <b>Save</b> button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99def5c2-3fc3-416c-80a6-6009927ab63e">SetOptions</a>
</td>
<td align="left" width="63%">
Sets flags to control the behavior of the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ae3d226-e825-443a-a2b0-4b5bb07fc9f7">SetTitle</a>
</td>
<td align="left" width="63%">
Sets the title of the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48504141-6612-43fe-8470-a9871b560f1a">Unadvise</a>
</td>
<td align="left" width="63%">
Removes an event handler that was attached through the <a href="https://msdn.microsoft.com/f5664a52-f26c-475d-84ef-0c657ae46e2e">IFileDialog::Advise</a> method.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>IFileDialog</b> is implemented by the common file dialog browser.




## -see-also




<a href="https://msdn.microsoft.com/f95b7106-18ab-4f7f-8d3f-267ac0293245">IFileOpenDialog</a>



<a href="https://msdn.microsoft.com/74021f92-54ff-4c02-a8cf-49bcd7b9171e">IFileSaveDialog</a>



<a href="https://msdn.microsoft.com/e9d640fd-ef10-486a-a037-01b7a71179a0">IModalWindow</a>
 

 

