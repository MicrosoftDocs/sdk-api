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

# DrawDibProfileDisplay function


## -description



The <b>DrawDibProfileDisplay</b> function determines settings for the display system when using DrawDib functions.




## -parameters




### -param lpbi

Pointer to a <a href="https://msdn.microsoft.com/153c08a8-d32c-4e9d-9da9-b915eb172327">BITMAPINFOHEADER</a> structure that contains bitmap information. You can also specify <b>NULL</b> to verify that the profile information is current. If the profile information is not current, DrawDib will rerun the profile tests to obtain a current set of information. When you call <b>DrawDibProfileDisplay</b> with this parameter set to <b>NULL</b>, the return value is meaningless.


## -returns




            Returns a value that indicates the fastest drawing and stretching capabilities of the display system. This value can be zero if the bitmap format is not supported or one or more of the following values.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PD_CAN_DRAW_DIB</b></dt>
</dl>
</td>
<td width="60%">
DrawDib can draw images using this format. Stretching might or might not also be supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PD_CAN_STRETCHDIB</b></dt>
</dl>
</td>
<td width="60%">
DrawDib can stretch and draw images using this format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PD_STRETCHDIB_1_1_OK</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a> draws unstretched images using this format faster than an alternative method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PD_STRETCHDIB_1_2_OK</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a> draws stretched images (in a 1:2 ratio) using this format faster than an alternative method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PD_STRETCHDIB_1_N_OK</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/3d57a79a-338d-48ab-8161-3ce17739bf20">StretchDIBits</a> draws stretched images (in a 1:N ratio) using this format faster than an alternative method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9ba47b8d-5328-477e-9272-21e897e54348">DrawDib Functions</a>
 

 

