---
UID: NF:ocidl.IPicture.get_Type
title: IPicture::get_Type method
author: windows-driver-content
description: Retrieves the current type of the picture contained in the picture object.
old-location: com\ipicture_get_type.htm
old-project: com
ms.assetid: b8c64bff-51a4-4b7d-bec4-56465933e96d
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IPicture, IPicture interface [COM], get_Type method, IPicture::get_Type, _ctrl_ipicture_get_type, com.ipicture_get_type, get_Type method [COM], get_Type method [COM], IPicture interface, get_Type,IPicture.get_Type, ocidl/IPicture::get_Type
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VIEWSTATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	OCIdl.h
api_name:
-	IPicture.get_Type
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPicture::get_Type method


## -description


Retrieves the current type of the picture contained in the picture object.


## -parameters




### -param pType [out]

Pointer to a variable that receives the picture type. The Type property can have any one of the values contained in the <a href="https://msdn.microsoft.com/79f10687-f0eb-4b5e-a1a9-9186dbd0b51f">PICTYPE</a> enumeration.


## -returns



This method supports the standard return value E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The type was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pType</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/42e3cd0e-2413-494a-8be8-2952089e02d2">IPicture</a>



<a href="https://msdn.microsoft.com/fb021348-07d4-4974-a71e-abb1b8d760c4">OleCreatePictureIndirect</a>



<a href="https://msdn.microsoft.com/79f10687-f0eb-4b5e-a1a9-9186dbd0b51f">PICTYPE</a>
 

 

