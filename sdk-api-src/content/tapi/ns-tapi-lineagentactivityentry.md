---
UID: NS:tapi.lineagentactivityentry_tag
title: LINEAGENTACTIVITYENTRY (tapi.h)
description: The LINEAGENTACTIVITYENTRY structure describes a single ACD agent activity. The LINEAGENTACTIVITYLIST structure can contain an array of LINEAGENTACTIVITYENTRY structures.
helpviewer_keywords: ["*LPLINEAGENTACTIVITYENTRY","LINEAGENTACTIVITYENTRY","LINEAGENTACTIVITYENTRY structure [TAPI 2.2]","LPLINEAGENTACTIVITYENTRY","LPLINEAGENTACTIVITYENTRY structure pointer [TAPI 2.2]","_tapi2_lineagentactivityentry_str","tapi/LINEAGENTACTIVITYENTRY","tapi/LPLINEAGENTACTIVITYENTRY","tapi2.lineagentactivityentry_str"]
old-location: tapi2\lineagentactivityentry_str.htm
tech.root: tapi3
ms.assetid: e4f869a9-608c-4119-863b-b29e8b0d9680
ms.date: 12/05/2018
ms.keywords: '*LPLINEAGENTACTIVITYENTRY, LINEAGENTACTIVITYENTRY, LINEAGENTACTIVITYENTRY structure [TAPI 2.2], LPLINEAGENTACTIVITYENTRY, LPLINEAGENTACTIVITYENTRY structure pointer [TAPI 2.2], _tapi2_lineagentactivityentry_str, tapi/LINEAGENTACTIVITYENTRY, tapi/LPLINEAGENTACTIVITYENTRY, tapi2.lineagentactivityentry_str'
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
req.typenames: LINEAGENTACTIVITYENTRY, *LPLINEAGENTACTIVITYENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineagentactivityentry_tag
 - tapi/lineagentactivityentry_tag
 - LPLINEAGENTACTIVITYENTRY
 - tapi/LPLINEAGENTACTIVITYENTRY
 - LINEAGENTACTIVITYENTRY
 - tapi/LINEAGENTACTIVITYENTRY
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
 - LINEAGENTACTIVITYENTRY
---

# LINEAGENTACTIVITYENTRY structure


## -description

The 
<b>LINEAGENTACTIVITYENTRY</b> structure describes a single ACD agent activity. The 
<a href="/windows/desktop/api/tapi/ns-tapi-lineagentactivitylist">LINEAGENTACTIVITYLIST</a> structure can contain an array of 
<b>LINEAGENTACTIVITYENTRY</b> structures.

## -struct-fields

### -field dwID

Unique identifier for an activity. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.

### -field dwNameSize

Size of the activity name including the <b>null</b> terminator, in bytes.

### -field dwNameOffset

Offset from the beginning of this structure to a <b>null</b>-terminated string specifying the name and other identifying information of an activity that can be selected by calling the 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentactivity">lineSetAgentActivity</a> function. The size of the string is specified by <b>dwNameSize</b>.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineagentactivitylist">LINEAGENTACTIVITYLIST</a>



<a href="/windows/desktop/api/tapi/ns-tapi-lineproxyrequest">LINEPROXYREQUEST</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetagentactivitylista">lineGetAgentActivityList</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentactivity">lineSetAgentActivity</a>