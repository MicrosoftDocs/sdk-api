---
UID: NN:shobjidl_core.IFileDialog
title: IFileDialog (shobjidl_core.h)
description: Exposes methods that initialize, show, and get results from the common file dialog.
old-location: shell\IFileDialog.htm
tech.root: shell
ms.assetid: 9341bb68-2410-4e03-8acd-fef29287b61c
ms.date: 12/05/2018
ms.keywords: IFileDialog, IFileDialog interface [Windows Shell], IFileDialog interface [Windows Shell],described, shell.IFileDialog, shell_IFileDialog, shobjidl_core/IFileDialog
ms.topic: interface
f1_keywords:
- shobjidl_core/IFileDialog
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- IFileDialog
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileDialog interface


## -description


Exposes methods that initialize, show, and get results from the common file dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileDialog</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow">IModalWindow</a>. <b>IFileDialog</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-addplace">AddPlace</a>
</td>
<td align="left" width="63%">
Adds a folder to the list of places available for the user to open or save items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise">Advise</a>
</td>
<td align="left" width="63%">
Assigns an event handler that listens for events coming from the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-clearclientdata">ClearClientData</a>
</td>
<td align="left" width="63%">
Instructs the dialog to clear all persisted state information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-close">Close</a>
</td>
<td align="left" width="63%">
Closes the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getcurrentselection">GetCurrentSelection</a>
</td>
<td align="left" width="63%">
Gets the user's current selection in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getfilename">GetFileName</a>
</td>
<td align="left" width="63%">
Retrieves the text currently entered in the dialog's <b>File name</b> edit box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb775958(v=vs.85)">GetFileTypeIndex</a>
</td>
<td align="left" width="63%">
Gets the currently selected file type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getfolder">GetFolder</a>
</td>
<td align="left" width="63%">
Gets either the folder currently selected in the dialog, or, if the dialog is not currently displayed, the folder that is to be selected when the dialog is opened.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions">GetOptions</a>
</td>
<td align="left" width="63%">
Gets the current flags that are set to control dialog behavior.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult">GetResult</a>
</td>
<td align="left" width="63%">
Gets the choice that the user made in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid">SetClientGuid</a>
</td>
<td align="left" width="63%">
Enables a calling application to associate a GUID with a dialog's persisted state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultextension">SetDefaultExtension</a>
</td>
<td align="left" width="63%">
Sets the default extension to be added to file names.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder">SetDefaultFolder</a>
</td>
<td align="left" width="63%">
Sets the folder used as a default if there is not a recently used folder value available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfilename">SetFileName</a>
</td>
<td align="left" width="63%">
Sets the file name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfilenamelabel">SetFileNameLabel</a>
</td>
<td align="left" width="63%">
Sets the text of the label next to the file name edit box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb775978(v=vs.85)">SetFileTypeIndex</a>
</td>
<td align="left" width="63%">
Sets the file type that appears as selected in the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes">SetFileTypes</a>
</td>
<td align="left" width="63%">
Sets the file types that the dialog can open or save.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfilter">SetFilter</a>
</td>
<td align="left" width="63%">
<b>Deprecated in Windows 7.</b> Sets the filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder">SetFolder</a>
</td>
<td align="left" width="63%">
Sets a folder that is always selected when the dialog is opened, regardless of previous user action.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setokbuttonlabel">SetOkButtonLabel</a>
</td>
<td align="left" width="63%">
Sets the text of the <b>Open</b> or <b>Save</b> button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions">SetOptions</a>
</td>
<td align="left" width="63%">
Sets flags to control the behavior of the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-settitle">SetTitle</a>
</td>
<td align="left" width="63%">
Sets the title of the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Removes an event handler that was attached through the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise">IFileDialog::Advise</a> method.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>IFileDialog</b> is implemented by the common file dialog browser.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog">IFileOpenDialog</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesavedialog">IFileSaveDialog</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow">IModalWindow</a>
 

 

