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

# IMSVidAnalogTuner2::get_TVFormats


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>get_TVFormats</b> method retrieves a flag value that indicates which TV formats the tuner supports, such as NTSC, PAL, or SECAM.


## -parameters




### -param Formats [out]

Pointer to a variable that receives the formats flag. Possible values are the sum of one or more of the values in the following table.

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
<td>0x00000000</td>
<td>Digital sensor</td>
</tr>
<tr>
<td>0x00000001</td>
<td>NTSC (M) standard, 7.5 IRE black</td>
</tr>
<tr>
<td>0x00000002</td>
<td>NTSC (M) standard, 0 IRE black (Japan)</td>
</tr>
<tr>
<td>0x00000004</td>
<td>NTSC-433</td>
</tr>
<tr>
<td>0x00000010</td>
<td>PAL-B standard</td>
</tr>
<tr>
<td>0x00000020</td>
<td>PAL (D) standard</td>
</tr>
<tr>
<td>0x00000080</td>
<td>PAL (H) standard</td>
</tr>
<tr>
<td>0x00000100</td>
<td>PAL (I) standard</td>
</tr>
<tr>
<td>0x00000200</td>
<td>PAL (M) standard</td>
</tr>
<tr>
<td>0x00000400</td>
<td>PAL (N) standard</td>
</tr>
<tr>
<td>0x00000800</td>
<td>PAL-60 standard</td>
</tr>
<tr>
<td>0x00001000</td>
<td>SECAM (B) standard</td>
</tr>
<tr>
<td>0x00002000</td>
<td>SECAM (D) standard</td>
</tr>
<tr>
<td>0x00004000</td>
<td>SECAM (G) standard</td>
</tr>
<tr>
<td>0x00008000</td>
<td>SECAM (H) standard</td>
</tr>
<tr>
<td>0x00010000</td>
<td>SECAM (K) standard</td>
</tr>
<tr>
<td>0x00020000</td>
<td>SECAM (K1) standard</td>
</tr>
<tr>
<td>0x00040000</td>
<td>SECAM (L) standard</td>
</tr>
<tr>
<td>0x00080000</td>
<td>SECAM (L1) standard</td>
</tr>
<tr>
<td>0x00100000</td>
<td>Combination (N) PAL standard (Argentina)</td>
</tr>
</table>
 


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/50d30a45-8cea-454c-b5d2-ff809b8a8206">IMSVidAnalogTuner2 Interface</a>
 

 

