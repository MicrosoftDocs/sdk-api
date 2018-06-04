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

# IWMImageInfo::GetImageCount


## -description



The <b>GetImageCount</b> method retrieves the number of images stored in a file using ID3v2 "APIC" frames. Images stored in the file using attributes in the Windows Media namespace, or any images stored in custom attributes, are not included in this count.




## -parameters




### -param pcImages [out]

Pointer to the number of images.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcImages</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
One of the ID3 frames that should be in the file cannot be accessed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1b3b4224-f86d-437c-969e-fe30e6d002a8">IWMImageInfo Interface</a>



<a href="https://msdn.microsoft.com/fe1dcd53-fcdd-4190-9a07-65d0b34112d0">IWMImageInfo::GetImage</a>
 

 

