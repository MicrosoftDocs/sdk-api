---
UID: NN:shobjidl_core.IFileSaveDialog
title: IFileSaveDialog (shobjidl_core.h)
author: windows-sdk-content
description: Extends the IFileDialog interface by adding methods specific to the save dialog, which include those that provide support for the collection of metadata to be persisted with the file.
old-location: shell\IFileSaveDialog.htm
tech.root: shell
ms.assetid: 74021f92-54ff-4c02-a8cf-49bcd7b9171e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFileSaveDialog, IFileSaveDialog interface [Windows Shell], IFileSaveDialog interface [Windows Shell],described, shell.IFileSaveDialog, shell_IFileSaveDialog, shobjidl_core/IFileSaveDialog
ms.topic: interface
f1_keywords: 
 - "shobjidl_core/IFileSaveDialog"
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
 - Shobjidl_core.h
api_name:
 - IFileSaveDialog
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileSaveDialog interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a> interface by adding methods specific to the save dialog, which include those that provide support for the collection of metadata to be persisted with the file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSaveDialog</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>. <b>IFileSaveDialog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileSaveDialog</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-applyproperties">ApplyProperties</a>
</td>
<td align="left" width="63%">
Applies a set of properties to an item using the Shell's copy engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb775685(v=vs.85)">GetOptions</a>
</td>
<td align="left" width="63%">
Gets the current flags that are set to control dialog behavior.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-getproperties">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves the set of property values for a saved item or an item in the process of being saved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-setcollectedproperties">SetCollectedProperties</a>
</td>
<td align="left" width="63%">
Specifies which properties will be collected in the save dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb775708(v=vs.85)">SetOptions</a>
</td>
<td align="left" width="63%">
Sets flags to control the behavior of the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-setproperties">SetProperties</a>
</td>
<td align="left" width="63%">
Provides a property store that defines the default values to be used for the item being saved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem">SetSaveAsItem</a>
</td>
<td align="left" width="63%">
Sets an item to be used as the initial entry in a <b>Save As</b> dialog.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a> interface, from which it inherits.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog">IFileDialog</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog">IFileOpenDialog</a>
 

 

