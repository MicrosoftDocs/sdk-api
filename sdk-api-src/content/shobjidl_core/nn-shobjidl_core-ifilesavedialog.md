---
UID: NN:shobjidl_core.IFileSaveDialog
title: IFileSaveDialog
author: windows-driver-content
description: Extends the IFileDialog interface by adding methods specific to the save dialog, which include those that provide support for the collection of metadata to be persisted with the file.
old-location: shell\IFileSaveDialog.htm
old-project: shell
ms.assetid: 74021f92-54ff-4c02-a8cf-49bcd7b9171e
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IFileSaveDialog, IFileSaveDialog interface [Windows Shell], IFileSaveDialog interface [Windows Shell],described, shell.IFileSaveDialog, shell_IFileSaveDialog, shobjidl_core/IFileSaveDialog
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl_core.h
api_name:
-	IFileSaveDialog
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# IFileSaveDialog interface


## -description


Extends the <a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a> interface by adding methods specific to the save dialog, which include those that provide support for the collection of metadata to be persisted with the file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileSaveDialog</b> interface inherits from <a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a>. <b>IFileSaveDialog</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3de64914-b64e-47e8-8f84-6c64d849ffa9">ApplyProperties</a>
</td>
<td align="left" width="63%">
Applies a set of properties to an item using the Shell's copy engine.

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
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991811">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves the set of property values for a saved item or an item in the process of being saved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cff40aba-6a87-4c20-957d-6729e0d995ae">SetCollectedProperties</a>
</td>
<td align="left" width="63%">
Specifies which properties will be collected in the save dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/064a412e-7fd5-4896-8c42-044aa53107a7">SetOptions</a>
</td>
<td align="left" width="63%">
Sets flags to control the behavior of the dialog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991815">SetProperties</a>
</td>
<td align="left" width="63%">
Provides a property store that defines the default values to be used for the item being saved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aa313685-1334-4899-a55a-6549b48e1464">SetSaveAsItem</a>
</td>
<td align="left" width="63%">
Sets an item to be used as the initial entry in a <b>Save As</b> dialog.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a> interface, from which it inherits.




## -see-also




<a href="https://msdn.microsoft.com/9341bb68-2410-4e03-8acd-fef29287b61c">IFileDialog</a>



<a href="https://msdn.microsoft.com/f95b7106-18ab-4f7f-8d3f-267ac0293245">IFileOpenDialog</a>
 

 

