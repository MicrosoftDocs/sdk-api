---
UID: NF:ocidl.IPicture.get_Width
title: IPicture::get_Width method
author: windows-driver-content
description: Retrieves the current width of the picture in the picture object.
old-location: com\ipicture_get_width.htm
old-project: com
ms.assetid: d69443ed-143c-4477-8602-50f919119b0f
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: IPicture, IPicture interface [COM], get_Width method, IPicture::get_Width, _ctrl_ipicture_get_width, com.ipicture_get_width, get_Width method [COM], get_Width method [COM], IPicture interface, get_Width,IPicture.get_Width, ocidl/IPicture::get_Width
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
-	IPicture.get_Width
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPicture::get_Width method


## -description


Retrieves the current width of the picture in the picture object.


## -parameters




### -param pWidth [out]

A pointer to a variable that receives the width.


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
The width was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pWidth</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/42e3cd0e-2413-494a-8be8-2952089e02d2">IPicture</a>
 

 

