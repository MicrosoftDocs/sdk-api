---
UID: NS:tapi.linequeueentry_tag
title: LINEQUEUEENTRY (tapi.h)
description: The LINEQUEUEENTRY structure provides the information for a single queue entry. The LINEQUEUELIST structure can contain an array of LINEQUEUEENTRY structures. This structure requires TAPI 3.0 version negotiation.
helpviewer_keywords: ["*LPLINEQUEUEENTRY","LINEQUEUEENTRY","LINEQUEUEENTRY structure [TAPI 2.2]","LPLINEQUEUEENTRY","LPLINEQUEUEENTRY structure pointer [TAPI 2.2]","_tapi2_linequeueentry","tapi/LINEQUEUEENTRY","tapi/LPLINEQUEUEENTRY","tapi2.linequeueentry"]
old-location: tapi2\linequeueentry.htm
tech.root: tapi3
ms.assetid: b05eb100-2a43-421f-826b-c37d05e4ef14
ms.date: 12/05/2018
ms.keywords: '*LPLINEQUEUEENTRY, LINEQUEUEENTRY, LINEQUEUEENTRY structure [TAPI 2.2], LPLINEQUEUEENTRY, LPLINEQUEUEENTRY structure pointer [TAPI 2.2], _tapi2_linequeueentry, tapi/LINEQUEUEENTRY, tapi/LPLINEQUEUEENTRY, tapi2.linequeueentry'
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
req.typenames: LINEQUEUEENTRY, *LPLINEQUEUEENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - linequeueentry_tag
 - tapi/linequeueentry_tag
 - LPLINEQUEUEENTRY
 - tapi/LPLINEQUEUEENTRY
 - LINEQUEUEENTRY
 - tapi/LINEQUEUEENTRY
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
 - LINEQUEUEENTRY
---

# LINEQUEUEENTRY structure


## -description

The 
<b>LINEQUEUEENTRY</b> structure provides the information for a single queue entry. The 
<a href="/windows/desktop/api/tapi/ns-tapi-linequeuelist">LINEQUEUELIST</a> structure can contain an array of 
<b>LINEQUEUEENTRY</b> structures. This structure requires TAPI 3.0 version negotiation.

## -struct-fields

### -field dwQueueID

Unique identifier for a queue. It is the responsibility of the agent handler to generate and maintain uniqueness of this identifier.

### -field dwNameSize

Size of the queue name string including the <b>null</b> terminator, in bytes.

### -field dwNameOffset

Offset from the beginning of the structure to a <b>null</b>-terminated string that specifies the name of the queue. The size of the string is specified by <b>dwNameSize</b>.

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linequeuelist">LINEQUEUELIST</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetqueuelista">lineGetQueueList</a>