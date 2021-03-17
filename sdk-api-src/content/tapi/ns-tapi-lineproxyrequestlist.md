---
UID: NS:tapi.lineproxyrequestlist_tag
title: LINEPROXYREQUESTLIST (tapi.h)
description: The LINEPROXYREQUESTLIST structure describes a list of proxy requests. The lineGetProxyStatus function returns the LINEPROXYREQUESTLIST structure.
helpviewer_keywords: ["*LPLINEPROXYREQUESTLIST","LINEPROXYREQUESTLIST","LINEPROXYREQUESTLIST structure [TAPI 2.2]","LPLINEPROXYREQUESTLIST","LPLINEPROXYREQUESTLIST structure pointer [TAPI 2.2]","_tapi2_lineproxyrequestlist","tapi/LINEPROXYREQUESTLIST","tapi/LPLINEPROXYREQUESTLIST","tapi2.lineproxyrequestlist"]
old-location: tapi2\lineproxyrequestlist.htm
tech.root: tapi3
ms.assetid: dc417954-56b4-4436-9582-7b656121fd6f
ms.date: 12/05/2018
ms.keywords: '*LPLINEPROXYREQUESTLIST, LINEPROXYREQUESTLIST, LINEPROXYREQUESTLIST structure [TAPI 2.2], LPLINEPROXYREQUESTLIST, LPLINEPROXYREQUESTLIST structure pointer [TAPI 2.2], _tapi2_lineproxyrequestlist, tapi/LINEPROXYREQUESTLIST, tapi/LPLINEPROXYREQUESTLIST, tapi2.lineproxyrequestlist'
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
req.typenames: LINEPROXYREQUESTLIST, *LPLINEPROXYREQUESTLIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineproxyrequestlist_tag
 - tapi/lineproxyrequestlist_tag
 - LPLINEPROXYREQUESTLIST
 - tapi/LPLINEPROXYREQUESTLIST
 - LINEPROXYREQUESTLIST
 - tapi/LINEPROXYREQUESTLIST
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
 - LINEPROXYREQUESTLIST
---

# LINEPROXYREQUESTLIST structure


## -description

The 
<b>LINEPROXYREQUESTLIST</b> structure describes a list of proxy requests. The 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetproxystatus">lineGetProxyStatus</a> function returns the 
<b>LINEPROXYREQUESTLIST</b> structure.

## -struct-fields

### -field dwTotalSize

Total size allocated to this structure, in bytes.

### -field dwNeededSize

Size needed to hold all the information requested, in bytes.

### -field dwUsedSize

Size of the portion of this structure that contains useful information, in bytes.

### -field dwNumEntries

Number of <b>DWORD</b> elements that appear in the list array.

### -field dwListSize

Size of the proxy request type list, in bytes.

### -field dwListOffset

Offset from the beginning of the structure to an array of <b>DWORD</b> elements indicating the currently supported proxy request types. Each element is one of the 
<a href="/windows/desktop/Tapi/lineproxyrequest--constants">LINEPROXYREQUEST_ constants</a>. The <b>dwListOffset</b> member is <b>dwNumEntries</b> times SIZEOF(DWORD). The size of the field is specified by <b>dwListSize</b>.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/Tapi/lineproxyrequest--constants">LINEPROXYREQUEST_ Constants</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetproxystatus">lineGetProxyStatus</a>