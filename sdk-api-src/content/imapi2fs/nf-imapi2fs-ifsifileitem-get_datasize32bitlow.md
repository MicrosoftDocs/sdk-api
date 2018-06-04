---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFsiFileItem::get_DataSize32BitLow


## -description


Retrieves the least significant 32 bits of the <a href="https://msdn.microsoft.com/e0e53ca9-bb72-4191-9025-d07030c59a51">IFsiFileItem::get_DataSize</a> property.


## -parameters




### -param pVal [out]

Least significant 32 bits of the <a href="https://msdn.microsoft.com/e0e53ca9-bb72-4191-9025-d07030c59a51">IFsiFileItem::get_DataSize</a> property.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -remarks



This property and <a href="https://msdn.microsoft.com/2f4f06e7-10a6-4aa0-b7b1-bf8799fcd41e">IFsiFileItem::get_DataSize32BitHigh</a> together  provide the size of the file as two 32-bit numbers for languages that do not support 64-bit values, such as VBScript and Visual Basic 6.




## -see-also




<a href="https://msdn.microsoft.com/13085b1f-4ff9-48ff-a9ae-9a1c5cb9a108">IFsiFileItem</a>



<a href="https://msdn.microsoft.com/e0e53ca9-bb72-4191-9025-d07030c59a51">IFsiFileItem::get_DataSize</a>
 

 

