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

# _timecode structure


## -description


The <b>TIMECODE</b> structure contains basic timecode frame count information.


## -struct-fields




### -field wFrameRate

Number of frames per second. Specify with one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ED_FORMAT_SMPTE_30"></a><a id="ed_format_smpte_30"></a><dl>
<dt><b>ED_FORMAT_SMPTE_30</b></dt>
</dl>
</td>
<td width="60%">
30 frames per second. 

</td>
</tr>
<tr>
<td width="40%"><a id="ED_FORMAT_SMPTE_30DROP"></a><a id="ed_format_smpte_30drop"></a><dl>
<dt><b>ED_FORMAT_SMPTE_30DROP</b></dt>
</dl>
</td>
<td width="60%">
30 frames per second drop frame (actual rate 29.97 fps). 

</td>
</tr>
<tr>
<td width="40%"><a id="ED_FORMAT_SMPTE_25"></a><a id="ed_format_smpte_25"></a><dl>
<dt><b>ED_FORMAT_SMPTE_25</b></dt>
</dl>
</td>
<td width="60%">
25 frames per second. 

</td>
</tr>
<tr>
<td width="40%"><a id="ED_FORMAT_SMPTE_24"></a><a id="ed_format_smpte_24"></a><dl>
<dt><b>ED_FORMAT_SMPTE_24</b></dt>
</dl>
</td>
<td width="60%">
24 frames per second. 

</td>
</tr>
</table>
 


### -field wFrameFract

Fractional frame. Full scale is 0x1000.


### -field dwFrames

Timecode value as a binary framecount.


### -field qw

 




## -remarks



Fractional frame can be used to indicate temporal offset into frame when timecode was actually read from an external device; for example, wFrameFract=0x7ff means the timecode value was read from the device at the end of the first video field. 




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

