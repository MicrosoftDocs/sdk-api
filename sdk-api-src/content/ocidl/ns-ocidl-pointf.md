---
UID: NS:ocidl.tagPOINTF
title: POINTF (ocidl.h)
description: Contains information that is used to convert between container units, expressed in floating point, and control units, expressed in HIMETRIC.
helpviewer_keywords: ["*LPPOINTF","LPPOINTF","LPPOINTF structure pointer [COM]","POINTF","POINTF structure [COM]","_ole_POINTF","com.pointf","ocidl/LPPOINTF","ocidl/POINTF"]
old-location: com\pointf.htm
tech.root: com
ms.assetid: 2b201df8-efee-4302-a93c-b514b982cf2b
ms.date: 12/05/2018
ms.keywords: '*LPPOINTF, LPPOINTF, LPPOINTF structure pointer [COM], POINTF, POINTF structure [COM], _ole_POINTF, com.pointf, ocidl/LPPOINTF, ocidl/POINTF'
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: POINTF, *LPPOINTF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPOINTF
 - ocidl/tagPOINTF
 - LPPOINTF
 - ocidl/LPPOINTF
 - POINTF
 - ocidl/POINTF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - POINTF
---

# POINTF structure


## -description

Contains information that is used to convert between container units, expressed in floating point, and control units, expressed in <b>HIMETRIC</b>. The <b>POINTF</b> structure specifically holds the floating point container units. Controls do not attempt to interpret either value in the structure.

## -struct-fields

### -field x

The x coordinates of the point in units that the container finds convenient.

### -field y

The y coordinates of the point in units that the container finds convenient.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-iolecontrolsite-transformcoords">IOleControlSite::TransformCoords</a>