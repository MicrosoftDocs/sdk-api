---
UID: NN:shobjidl_core.IFileDialogEvents
title: IFileDialogEvents (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods that allow notification of events within a common file dialog.
old-location: shell\IFileDialogEvents.htm
tech.root: shell
ms.assetid: c55107a3-ae0a-4b46-80a3-8a731b47976c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFileDialogEvents, IFileDialogEvents interface [Windows Shell], IFileDialogEvents interface [Windows Shell],described, shell.IFileDialogEvents, shell_IFileDialogEvents, shobjidl_core/IFileDialogEvents
ms.topic: interface
f1_keywords: ["shobjidl_core/IFileDialogEvents"]
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IFileDialogEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileDialogEvents interface


## -description


Exposes methods that allow notification of events within a common file dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileDialogEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileDialogEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileDialogEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok">OnFileOk</a>
</td>
<td align="left" width="63%">
Called just before the dialog is about to return with a result.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfolderchange">OnFolderChange</a>
</td>
<td align="left" width="63%">
Called when the user navigates to a new folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfolderchanging">OnFolderChanging</a>
</td>
<td align="left" width="63%">
Called before <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfolderchange">IFileDialogEvents::OnFolderChange</a>. This allows the implementer to stop navigation to a particular location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onoverwrite">OnOverwrite</a>
</td>
<td align="left" width="63%">
Called from the save dialog when the user chooses to overwrite a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onselectionchange">OnSelectionChange</a>
</td>
<td align="left" width="63%">
Called when the user changes the selection in the dialog's view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onshareviolation">OnShareViolation</a>
</td>
<td align="left" width="63%">
Enables an application to respond to sharing violations that arise from Open or Save operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-ontypechange">OnTypeChange</a>
</td>
<td align="left" width="63%">
Called when the dialog is opened to notify the application of the initial chosen filetype.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
<b>IFileDialogEvents</b> is implemented by an application that is a client of the common file dialog browser. Methods that are not implemented should return E_NOTIMPL. An example of <b>IFileDialogEvents</b> can be found in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd940349(v=vs.85)">Common File Dialog</a> SDK sample.



