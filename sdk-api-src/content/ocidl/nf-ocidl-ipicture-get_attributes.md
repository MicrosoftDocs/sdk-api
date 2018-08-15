---
UID: NF:ocidl.IPicture.get_Attributes
title: IPicture::get_Attributes
author: windows-sdk-content
description: Retrieves the current set of the picture's bit attributes.
old-location: com\ipicture_get_attributes.htm
old-project: com
ms.assetid: ed71f0eb-3af4-463f-93e1-29d5dd1cc684
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPicture interface [COM],get_Attributes method, IPicture.get_Attributes, IPicture::get_Attributes, _ctrl_ipicture_get_attributes, com.ipicture_get_attributes, get_Attributes, get_Attributes method [COM], get_Attributes method [COM],IPicture interface, ocidl/IPicture::get_Attributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ocidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VIEWSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPicture.get_Attributes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPicture::get_Attributes


## -description


Retrieves the current set of the picture's bit attributes.


## -parameters




### -param pDwAttr [out]

A pointer to a variable that receives the value of the Attributes property.

The Attributes property can contain any combination of the values from the <a href="https://msdn.microsoft.com/3162a305-d35c-402d-a8d8-f0f124257dd5">PICTUREATTRIBUTES</a> enumeration.


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
The attribute bits were returned successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>pdwAttr</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/42e3cd0e-2413-494a-8be8-2952089e02d2">IPicture</a>



<a href="https://msdn.microsoft.com/3162a305-d35c-402d-a8d8-f0f124257dd5">PICTUREATTRIBUTES</a>
 

 

