---
UID: NN:shldisp.IShellFolderViewDual
title: IShellFolderViewDual (shldisp.h)
description: Exposes methods that modify the view and select items in the current folder.
helpviewer_keywords: ["IShellFolderViewDual","IShellFolderViewDual interface [Windows Shell]","IShellFolderViewDual interface [Windows Shell]","described","_shell_IShellFolderViewDual","shell.IShellFolderViewDual","shldisp/IShellFolderViewDual"]
old-location: shell\IShellFolderViewDual.htm
tech.root: shell
ms.assetid: 48135f9d-ee80-4dec-87dc-83f407c25777
ms.date: 12/05/2018
ms.keywords: IShellFolderViewDual, IShellFolderViewDual interface [Windows Shell], IShellFolderViewDual interface [Windows Shell],described, _shell_IShellFolderViewDual, shell.IShellFolderViewDual, shldisp/IShellFolderViewDual
f1_keywords:
- shldisp/IShellFolderViewDual
dev_langs:
- c++
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
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
- Shldisp.h
api_name:
- IShellFolderViewDual
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IShellFolderViewDual interface


## -description


Exposes methods that modify the view and select items in the current folder.
		


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellFolderViewDual</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IShellFolderViewDual</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellFolderViewDual</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual-get_application">get_Application</a>
</td>
<td align="left" width="63%">
Gets the application object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual-get_focuseditem">get_FocusedItem</a>
</td>
<td align="left" width="63%">
Gets the FolderItem object that represents the item that has input focus.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual-get_folder">get_Folder</a>
</td>
<td align="left" width="63%">
Gets the Folder object that represents the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual-get_parent">get_Parent</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual-get_script">get_Script</a>
</td>
<td align="left" width="63%">
Gets the scripting object for the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual-get_viewoptions">get_ViewOptions</a>
</td>
<td align="left" width="63%">
Gets a set of flags that indicate the current options of the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual-popupitemmenu">PopupItemMenu</a>
</td>
<td align="left" width="63%">
Creates a shortcut menu for the specified item and returns the selected command string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual-selecteditems">SelectedItems</a>
</td>
<td align="left" width="63%">
Gets a FolderItems object that represents all of the selected items in the view.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nf-shldisp-ishellfolderviewdual-selectitem">SelectItem</a>
</td>
<td align="left" width="63%">
Sets the selection state of an item in the view.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual2">IShellFolderViewDual2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shldisp/nn-shldisp-ishellfolderviewdual3">IShellFolderViewDual3</a>
 

 

