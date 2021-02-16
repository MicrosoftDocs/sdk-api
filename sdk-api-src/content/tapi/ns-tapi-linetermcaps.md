---
UID: NS:tapi.linetermcaps_tag
title: LINETERMCAPS (tapi.h)
description: The LINETERMCAPS structure describes the capabilities of a line's terminal device. The LINEDEVCAPS structure can contain an array of LINETERMCAPS structures.
helpviewer_keywords: ["*LPLINETERMCAPS","LINETERMCAPS","LINETERMCAPS structure [TAPI 2.2]","LPLINETERMCAPS","LPLINETERMCAPS structure pointer [TAPI 2.2]","_tapi2_linetermcaps_str","tapi/LINETERMCAPS","tapi/LPLINETERMCAPS","tapi2.linetermcaps_str"]
old-location: tapi2\linetermcaps_str.htm
tech.root: tapi3
ms.assetid: 54d36126-a032-4baa-8484-6ebeb9c4adf9
ms.date: 12/05/2018
ms.keywords: '*LPLINETERMCAPS, LINETERMCAPS, LINETERMCAPS structure [TAPI 2.2], LPLINETERMCAPS, LPLINETERMCAPS structure pointer [TAPI 2.2], _tapi2_linetermcaps_str, tapi/LINETERMCAPS, tapi/LPLINETERMCAPS, tapi2.linetermcaps_str'
req.header: tapi.h
req.include-header: 
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
req.typenames: LINETERMCAPS, *LPLINETERMCAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linetermcaps_tag
 - tapi/linetermcaps_tag
 - LPLINETERMCAPS
 - tapi/LPLINETERMCAPS
 - LINETERMCAPS
 - tapi/LINETERMCAPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - LINETERMCAPS
---

# LINETERMCAPS structure


## -description

The 
<b>LINETERMCAPS</b> structure describes the capabilities of a line's terminal device. The 
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure can contain an array of 
<b>LINETERMCAPS</b> structures.

## -struct-fields

### -field dwTermDev

Device type of the terminal. This member uses one of the 
<a href="/windows/desktop/Tapi/linetermdev--constants">LINETERMDEV_ Constants</a>.

### -field dwTermModes

Terminal mode(s) the terminal device is able to deal with. This member uses one of the 
<a href="/windows/desktop/Tapi/linetermmode--constants">LINETERMMODE_ Constants</a>.

### -field dwTermSharing

Sharing modes for the terminal device. This member uses one of the 
<a href="/windows/desktop/Tapi/linetermsharing--constants">LINETERMSHARING_ Constants</a>.

## -remarks

This structure may not be extended.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetdevcaps">TSPI_lineGetDevCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetdevcaps">lineGetDevCaps</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetterminal">lineSetTerminal</a>