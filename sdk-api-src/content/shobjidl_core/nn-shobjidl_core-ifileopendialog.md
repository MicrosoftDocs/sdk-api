---
UID: NN:shobjidl_core.IFileOpenDialog
title: IFileOpenDialog
author: windows-sdk-content
description: Extends the IFileDialog interface by adding methods specific to the open dialog.
old-location: shell\IFileOpenDialog.htm
tech.root: Shell
ms.assetid: f95b7106-18ab-4f7f-8d3f-267ac0293245
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IFileOpenDialog, IFileOpenDialog interface [Windows Shell], IFileOpenDialog interface [Windows Shell],described, shell.IFileOpenDialog, shell_IFileOpenDialog, shobjidl_core/IFileOpenDialog
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOpenDialog interface


## -description


Extends the <a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a> interface by adding methods specific to the open dialog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileOpenDialog</b> interface inherits from <a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a>. <b>IFileOpenDialog</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5c710dae-4988-4f19-beb5-2ff9cd11c596">GetResults</a>
</td>
<td align="left" width="63%">
Gets the user's choices in a dialog that allows multiple selection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fc53607-60d2-4d23-b11e-779c26c02b0f">GetSelectedItems</a>
</td>
<td align="left" width="63%">
Gets the currently selected items in the dialog. These items may be items selected in the view, or text selected in the file name edit box.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a> interface, from which it inherits.




## -see-also




<a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a>



<a href="https://msdn.microsoft.com/74021f92-54ff-4c02-a8cf-49bcd7b9171e">IFileSaveDialog</a>
 

 

