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

# IWMCodecStrings::GetName


## -description



Retrieves the name of a codec.



## -parameters




### -param pmt [in]

Pointer to the output media type. If <b>NULL</b>, the codec will use the media type that is currently set.


### -param cchLength [in]

Size of szName buffer in wide characters.


### -param szName [out]

Address of the wide-character buffer that receives the name. If <b>NULL</b>, pcchLength receives the required length.


### -param pcchLength [out]

Pointer to the required buffer length in wide characters, including the null terminating character.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/84b6223e-d42a-47b0-8553-2b4d69de2da3">IWMCodecStrings Interface</a>
 

 

