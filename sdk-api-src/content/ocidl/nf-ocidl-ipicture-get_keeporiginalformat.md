---
UID: NF:ocidl.IPicture.get_KeepOriginalFormat
title: IPicture::get_KeepOriginalFormat
author: windows-sdk-content
description: Retrieves the current value of the picture's KeepOriginalFormat property.
old-location: com\ipicture_get_keeporiginalformat.htm
tech.root: com
ms.assetid: 90befcb7-138f-4c63-a6ec-ec06c89b3317
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IPicture interface [COM],get_KeepOriginalFormat method, IPicture.get_KeepOriginalFormat, IPicture::get_KeepOriginalFormat, _ctrl_ipicture_get_keeporiginalformat, com.ipicture_get_keeporiginalformat, get_KeepOriginalFormat, get_KeepOriginalFormat method [COM], get_KeepOriginalFormat method [COM],IPicture interface, ocidl/IPicture::get_KeepOriginalFormat
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPicture.get_KeepOriginalFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPicture::get_KeepOriginalFormat


## -description


Retrieves the current value of the picture's KeepOriginalFormat property.


## -parameters




### -param pKeep [out]

A pointer to a variable that receives the value of the property.


## -returns



This method supports the standard return value E_FAIL, as well as the following value.

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
The value of the KeepOriginalFormat property was returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pKeep</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/42e3cd0e-2413-494a-8be8-2952089e02d2">IPicture</a>



<a href="https://msdn.microsoft.com/04d952cf-a3c0-4220-9d24-8188ce52f862">IPicture::put_KeepOriginalFormat</a>
 

 

