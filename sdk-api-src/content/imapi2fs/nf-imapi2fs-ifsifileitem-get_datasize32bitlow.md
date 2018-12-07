---
UID: NF:imapi2fs.IFsiFileItem.get_DataSize32BitLow
title: IFsiFileItem::get_DataSize32BitLow
author: windows-sdk-content
description: Retrieves the least significant 32 bits of the IFsiFileItem::get_DataSize property.
old-location: imapi\ifsifileitem_get_datasize32bitlow.htm
tech.root: imapi
ms.assetid: beeec2bc-5f0e-4a53-afed-50c0b6069f54
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsiFileItem interface [IMAPI],get_DataSize32BitLow method, IFsiFileItem.get_DataSize32BitLow, IFsiFileItem::get_DataSize32BitLow, get_DataSize32BitLow, get_DataSize32BitLow method [IMAPI], get_DataSize32BitLow method [IMAPI],IFsiFileItem interface, imapi.ifsifileitem_get_datasize32bitlow, imapi2fs/IFsiFileItem::get_DataSize32BitLow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - imapi2fs.h
api_name:
 - IFsiFileItem.get_DataSize32BitLow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

