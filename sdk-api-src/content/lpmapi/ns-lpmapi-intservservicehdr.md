---
UID: NS:lpmapi.IntServServiceHdr
title: IntServServiceHdr (lpmapi.h)
description: The IntServServiceHdr structure is a header for Integrated Services service objects.
helpviewer_keywords: ["IntServServiceHdr","IntServServiceHdr structure [QOS]","lpmapi/IntServServiceHdr","qos.intservservicehdr"]
old-location: qos\intservservicehdr.htm
tech.root: QOS
ms.assetid: 63e6a944-f16e-4b90-ab77-22e5c8ef3fb2
ms.date: 12/05/2018
ms.keywords: IntServServiceHdr, IntServServiceHdr structure [QOS], lpmapi/IntServServiceHdr, qos.intservservicehdr
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
req.typenames: IntServServiceHdr
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IntServServiceHdr
 - lpmapi/IntServServiceHdr
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
 - IntServServiceHdr
---

# IntServServiceHdr structure


## -description

The 
<b>IntServServiceHdr</b> structure is a header for Integrated Services service objects.

## -struct-fields

### -field issh_service

Service number of the attached object.

### -field issh_flags

Flags for the corresponding service object.

### -field issh_len32b

Number of 32-bit WORDs in the object, excluding this header object.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservmainhdr">IntServMainHdr</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-intservparmhdr">IntServParmHdr</a>

