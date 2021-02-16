---
UID: NS:drt.drt_registration_tag
title: DRT_REGISTRATION (drt.h)
description: The DRT_REGISTRATION structure contains key and application data that make up a registration.
helpviewer_keywords: ["*PDRT_REGISTRATION","DRT_REGISTRATION","DRT_REGISTRATION structure [Peer Networking]","PDRT_REGISTRATION","PDRT_REGISTRATION structure pointer [Peer Networking]","drt/DRT_REGISTRATION","drt/PDRT_REGISTRATION","p2p.drt_registration"]
old-location: p2p\drt_registration.htm
tech.root: p2p
ms.assetid: 1b5fea2c-c1df-4639-8f62-e62d8a09b1f5
ms.date: 12/05/2018
ms.keywords: '*PDRT_REGISTRATION, DRT_REGISTRATION, DRT_REGISTRATION structure [Peer Networking], PDRT_REGISTRATION, PDRT_REGISTRATION structure pointer [Peer Networking], drt/DRT_REGISTRATION, drt/PDRT_REGISTRATION, p2p.drt_registration'
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DRT_REGISTRATION, *PDRT_REGISTRATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - drt_registration_tag
 - drt/drt_registration_tag
 - PDRT_REGISTRATION
 - drt/PDRT_REGISTRATION
 - DRT_REGISTRATION
 - drt/DRT_REGISTRATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_REGISTRATION
---

# DRT_REGISTRATION structure


## -description

The <b>DRT_REGISTRATION</b> structure contains  key and application data that make up a registration.

## -struct-fields

### -field key

Contains the key portion of the registration.

### -field appData

The application data associated with the key. The <a href="/windows/desktop/api/drt/ns-drt-drt_data">DRT_DATA</a> structure containing this application data must point to a buffer less than 4KB in size.

## -see-also

<a href="/windows/desktop/api/drt/ns-drt-drt_search_result">DRT_SEARCH_RESULT</a>



<a href="/windows/desktop/api/drt/nf-drt-drtcreatederivedkey">DrtCreateDerivedKey</a>



<a href="/windows/desktop/api/drt/nf-drt-drtregisterkey">DrtRegisterKey</a>