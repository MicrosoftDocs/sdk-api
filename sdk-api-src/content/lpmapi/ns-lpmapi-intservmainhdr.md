---
UID: NS:lpmapi.IntServMainHdr
title: IntServMainHdr (lpmapi.h)
description: The IntServMainHdr structure is a header for Integrated Services RSVP objects.
helpviewer_keywords: ["IntServMainHdr","IntServMainHdr structure [QOS]","lpmapi/IntServMainHdr","qos.intservmainhdr"]
old-location: qos\intservmainhdr.htm
tech.root: QOS
ms.assetid: b67fdf53-322b-4a70-ae83-63d4365e9b57
ms.date: 12/05/2018
ms.keywords: IntServMainHdr, IntServMainHdr structure [QOS], lpmapi/IntServMainHdr, qos.intservmainhdr
req.header: lpmapi.h
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
req.typenames: IntServMainHdr
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IntServMainHdr
 - lpmapi/IntServMainHdr
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - IntServMainHdr
---

# IntServMainHdr structure


## -description

The 
<b>IntServMainHdr</b> structure is a header for Integrated Services RSVP objects.

## -struct-fields

### -field ismh_version

Version of this header.

### -field ismh_unused

Reserved. Do not use.

### -field ismh_len32b

Number of 32-bit WORDs in the object, excluding this header object.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservservicehdr">IntServServiceHdr</a>

