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

# IDVRGB219::SetRGB219


## -description



The <code>SetRGB219</code> method controls the dynamic range for DV encoding and decoding.



The DV video format has a dynamic range of 16–235. By default, when the DV Video Decoder decodes to 24-bit or 32-bit RGB, it stretches the color range to 0–255. Similarly, the DV Video Encoder compresses 24-bit RGB into the 16-235 range. In RGB-219 mode, the decoder does not stretch the color range, and the encoder does not compress the color range. Use the <code>SetRGB219</code> method to toggle between the default mode and RGB-219 mode.


## -parameters




### -param bState [in]

Boolean value that specifies the filter's encoding or decoder behavior.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Enable RGB-219 mode.</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Disable RGB-219 mode. Use the default mode.</td>
</tr>
</table>
 


## -returns



Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> failure code.




## -remarks



For the encoder, this method has no effect unless the input type is RGB-24. For the decoder, it has no effect unless the output type is RGB-24 or RGB-32.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6d346f0b-97c1-4f3c-aa79-b3bfab18c634">IDVRGB219 Interface</a>
 

 

