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

# _DDSKIPNEXTFIELDINFO structure


## -description


The DDSKIPNEXTFIELDINFO structure contains the skip information for the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object. 


## -struct-fields




### -field lpVideoPortData

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550395">DDVIDEOPORTDATA</a> structure that represents the VPE object. 


### -field dwSkipFlags

Indicates whether to skip the next field. One of the following: 

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDSKIP_ENABLENEXT

</td>
<td>
The next field should be restored.

</td>
</tr>
<tr>
<td>
DDSKIP_SKIPNEXT

</td>
<td>
The next field should be skipped.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550395">DDVIDEOPORTDATA</a>



<a href="https://msdn.microsoft.com/da19c8dc-fef5-41e6-b032-2a0ae05a73da">DxSkipNextField</a>
 

 

