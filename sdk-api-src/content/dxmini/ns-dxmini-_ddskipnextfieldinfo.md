---
UID: NS:dxmini._DDSKIPNEXTFIELDINFO
title: "_DDSKIPNEXTFIELDINFO"
author: windows-sdk-content
description: The DDSKIPNEXTFIELDINFO structure contains the skip information for the video port extensions (VPE) object.
old-location: display\ddskipnextfieldinfo.htm
tech.root: display
ms.assetid: ae9de986-ed63-4c39-b882-e57cdda31863
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PDDSKIPNEXTFIELDINFO, DDSKIPNEXTFIELDINFO, DDSKIPNEXTFIELDINFO structure [Display Devices], PDDSKIPNEXTFIELDINFO, PDDSKIPNEXTFIELDINFO structure pointer [Display Devices], Video_Structs_13064c2a-b18d-467e-8aa9-0fbc6241eb99.xml, _DDSKIPNEXTFIELDINFO, display.ddskipnextfieldinfo, dxmini/DDSKIPNEXTFIELDINFO, dxmini/PDDSKIPNEXTFIELDINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxmini.h
req.include-header: Dxmini.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDSKIPNEXTFIELDINFO
product: Windows
targetos: Windows
req.typenames: DDSKIPNEXTFIELDINFO, *PDDSKIPNEXTFIELDINFO
req.redist: 
---

# _DDSKIPNEXTFIELDINFO structure


## -description


The DDSKIPNEXTFIELDINFO structure contains the skip information for the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> object. 


## -struct-fields




### -field lpVideoPortData

Points to a <a href="https://msdn.microsoft.com/662ff6ee-d6b1-4cb1-8ff8-b4c1e17b26df">DDVIDEOPORTDATA</a> structure that represents the VPE object. 


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




<a href="https://msdn.microsoft.com/662ff6ee-d6b1-4cb1-8ff8-b4c1e17b26df">DDVIDEOPORTDATA</a>



<a href="https://msdn.microsoft.com/da19c8dc-fef5-41e6-b032-2a0ae05a73da">DxSkipNextField</a>
 

 

