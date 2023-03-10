---
UID: NS:tapi.linecallhubtrackinginfo_tag
title: LINECALLHUBTRACKINGINFO (tapi.h)
description: The LINECALLHUBTRACKINGINFO structure contains information that reports the type of tracking available to a call hub. This structure is exposed only to applications that negotiate a TAPI version of 2.2 or higher.
helpviewer_keywords: ["*LPLINECALLHUBTRACKINGINFO","LINECALLHUBTRACKINGINFO","LINECALLHUBTRACKINGINFO structure [TAPI 2.2]","LPLINECALLHUBTRACKINGINFO","LPLINECALLHUBTRACKINGINFO structure pointer [TAPI 2.2]","_tapi2_linecallhubtrackinginfo_str","tapi/LINECALLHUBTRACKINGINFO","tapi/LPLINECALLHUBTRACKINGINFO","tapi2.linecallhubtrackinginfo_str"]
old-location: tapi2\linecallhubtrackinginfo_str.htm
tech.root: tapi3
ms.assetid: 1f4eaf7d-fc80-4131-af5a-30c6869c74ef
ms.date: 12/05/2018
ms.keywords: '*LPLINECALLHUBTRACKINGINFO, LINECALLHUBTRACKINGINFO, LINECALLHUBTRACKINGINFO structure [TAPI 2.2], LPLINECALLHUBTRACKINGINFO, LPLINECALLHUBTRACKINGINFO structure pointer [TAPI 2.2], _tapi2_linecallhubtrackinginfo_str, tapi/LINECALLHUBTRACKINGINFO, tapi/LPLINECALLHUBTRACKINGINFO, tapi2.linecallhubtrackinginfo_str'
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
req.typenames: LINECALLHUBTRACKINGINFO, *LPLINECALLHUBTRACKINGINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linecallhubtrackinginfo_tag
 - tapi/linecallhubtrackinginfo_tag
 - LPLINECALLHUBTRACKINGINFO
 - tapi/LPLINECALLHUBTRACKINGINFO
 - LINECALLHUBTRACKINGINFO
 - tapi/LINECALLHUBTRACKINGINFO
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
 - LINECALLHUBTRACKINGINFO
---

# LINECALLHUBTRACKINGINFO structure


## -description

The 
<b>LINECALLHUBTRACKINGINFO</b> structure contains information that reports the type of tracking available to a call hub. This structure is exposed only to applications that negotiate a TAPI version of 2.2 or higher.

The 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetcallhubtracking">TSPI_lineSetCallHubTracking</a> function and the 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallhubtracking">TSPI_lineGetCallHubTracking</a> function use the 
<b>LINECALLHUBTRACKINGINFO</b> structure.

## -struct-fields

### -field dwTotalSize

Total size, in bytes.

### -field dwNeededSize

Size needed, in bytes.

### -field dwUsedSize

Size used, in bytes.

### -field dwAvailableTracking

Available tracking, as represented by a 
<a href="/windows/desktop/Tapi/linecallhubtracking--constants">LINECALLHUBTRACKING</a>.constant.

### -field dwCurrentTracking

Current tracking, as represented by a <a href="/windows/desktop/Tapi/linecallhubtracking--constants">LINECALLHUBTRACKING</a> constant.

## -see-also

<a href="/windows/desktop/Tapi/linecallhubtracking--constants">LINECALLHUBTRACKING</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linegetcallhubtracking">TSPI_lineGetCallHubTracking</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linesetcallhubtracking">TSPI_lineSetCallHubTracking</a>