---
UID: NN:shobjidl_core.IFileOpenDialog
title: IFileOpenDialog (shobjidl_core.h)
description: Extends the IFileDialog interface by adding methods specific to the open dialog.
old-location: shell\IFileOpenDialog.htm
tech.root: shell
ms.assetid: f95b7106-18ab-4f7f-8d3f-267ac0293245
ms.date: 12/05/2018
ms.keywords: IFileOpenDialog, IFileOpenDialog interface [Windows Shell], IFileOpenDialog interface [Windows Shell],described, shell.IFileOpenDialog, shell_IFileOpenDialog, shobjidl_core/IFileOpenDialog
f1_keywords:
- shobjidl_core/IFileOpenDialog
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
- IFileOpenDialog
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileOpenDialog interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a> interface by adding methods specific to the open dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileOpenDialog</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>. <b>IFileOpenDialog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileOpenDialog</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults">GetResults</a>
</td>
<td align="left" width="63%">
Gets the user's choices in a dialog that allows multiple selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getselecteditems">GetSelectedItems</a>
</td>
<td align="left" width="63%">
Gets the currently selected items in the dialog. These items may be items selected in the view, or text selected in the file name edit box.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a> interface, from which it inherits.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifilesavedialog">IFileSaveDialog</a>
 

 

