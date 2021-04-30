---
UID: NS:tapi.linecalllist_tag
title: LINECALLLIST (tapi.h)
description: The LINECALLLIST structure describes a list of call handles. A structure of this type is returned by the lineGetNewCalls and lineGetConfRelatedCalls functions.
helpviewer_keywords: ["*LPLINECALLLIST","LINECALLLIST","LINECALLLIST structure [TAPI 2.2]","LPLINECALLLIST","LPLINECALLLIST structure pointer [TAPI 2.2]","_tapi2_linecalllist_str","tapi/LINECALLLIST","tapi/LPLINECALLLIST","tapi2.linecalllist_str"]
old-location: tapi2\linecalllist_str.htm
tech.root: tapi3
ms.assetid: b715dd07-74bd-4267-91fe-cfc0cd1e6aa4
ms.date: 12/05/2018
ms.keywords: '*LPLINECALLLIST, LINECALLLIST, LINECALLLIST structure [TAPI 2.2], LPLINECALLLIST, LPLINECALLLIST structure pointer [TAPI 2.2], _tapi2_linecalllist_str, tapi/LINECALLLIST, tapi/LPLINECALLLIST, tapi2.linecalllist_str'
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
req.typenames: LINECALLLIST, *LPLINECALLLIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linecalllist_tag
 - tapi/linecalllist_tag
 - LPLINECALLLIST
 - tapi/LPLINECALLLIST
 - LINECALLLIST
 - tapi/LINECALLLIST
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
 - LINECALLLIST
---

# LINECALLLIST structure


## -description

The 
<b>LINECALLLIST</b> structure describes a list of call handles. A structure of this type is returned by the 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetnewcalls">lineGetNewCalls</a> and 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetconfrelatedcalls">lineGetConfRelatedCalls</a> functions.

## -struct-fields

### -field dwTotalSize

Total size allocated to this data structure, in bytes.

### -field dwNeededSize

Size for this data structure that is needed to hold all the returned information, in bytes.

### -field dwUsedSize

Size of the portion of this data structure that contains useful information, in bytes.

### -field dwCallsNumEntries

Number of handles in the <i>hCalls</i> array.

### -field dwCallsSize

Size of the array of call handles, in bytes.

### -field dwCallsOffset

Offset from the beginning of the structure to the variably sized array of <b>HCALL</b> handles. The size of the array is specified by <b>dwCallsSize</b>.

## -remarks

This structure may not be extended.

## -see-also

<a href="/windows/desktop/api/tapi/nf-tapi-linegetconfrelatedcalls">lineGetConfRelatedCalls</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetnewcalls">lineGetNewCalls</a>