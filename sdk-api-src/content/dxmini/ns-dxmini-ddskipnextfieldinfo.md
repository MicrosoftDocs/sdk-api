---
UID: NS:dxmini._DDSKIPNEXTFIELDINFO
title: DDSKIPNEXTFIELDINFO (dxmini.h)
description: The DDSKIPNEXTFIELDINFO structure contains the skip information for the video port extensions (VPE) object.
helpviewer_keywords: ["*PDDSKIPNEXTFIELDINFO","DDSKIPNEXTFIELDINFO","DDSKIPNEXTFIELDINFO structure [Display Devices]","PDDSKIPNEXTFIELDINFO","PDDSKIPNEXTFIELDINFO structure pointer [Display Devices]","Video_Structs_13064c2a-b18d-467e-8aa9-0fbc6241eb99.xml","display.ddskipnextfieldinfo","dxmini/DDSKIPNEXTFIELDINFO","dxmini/PDDSKIPNEXTFIELDINFO"]
old-location: display\ddskipnextfieldinfo.htm
tech.root: display
ms.assetid: ae9de986-ed63-4c39-b882-e57cdda31863
ms.date: 12/05/2018
ms.keywords: '*PDDSKIPNEXTFIELDINFO, DDSKIPNEXTFIELDINFO, DDSKIPNEXTFIELDINFO structure [Display Devices], PDDSKIPNEXTFIELDINFO, PDDSKIPNEXTFIELDINFO structure pointer [Display Devices], Video_Structs_13064c2a-b18d-467e-8aa9-0fbc6241eb99.xml, display.ddskipnextfieldinfo, dxmini/DDSKIPNEXTFIELDINFO, dxmini/PDDSKIPNEXTFIELDINFO'
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
targetos: Windows
req.typenames: DDSKIPNEXTFIELDINFO, *PDDSKIPNEXTFIELDINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDSKIPNEXTFIELDINFO
 - dxmini/_DDSKIPNEXTFIELDINFO
 - PDDSKIPNEXTFIELDINFO
 - dxmini/PDDSKIPNEXTFIELDINFO
 - DDSKIPNEXTFIELDINFO
 - dxmini/DDSKIPNEXTFIELDINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxmini.h
api_name:
 - DDSKIPNEXTFIELDINFO
---

# DDSKIPNEXTFIELDINFO structure


## -description

The DDSKIPNEXTFIELDINFO structure contains the skip information for the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a> object.

## -struct-fields

### -field lpVideoPortData

Points to a <a href="/windows/desktop/api/dxmini/ns-dxmini-ddvideoportdata">DDVIDEOPORTDATA</a> structure that represents the VPE object.

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

<a href="/windows/desktop/api/dxmini/ns-dxmini-ddvideoportdata">DDVIDEOPORTDATA</a>



<a href="/windows/desktop/api/dxmini/nc-dxmini-pdx_skipnextfield">DxSkipNextField</a>