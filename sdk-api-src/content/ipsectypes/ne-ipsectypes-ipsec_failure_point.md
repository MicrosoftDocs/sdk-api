---
UID: NE:ipsectypes.IPSEC_FAILURE_POINT_
title: IPSEC_FAILURE_POINT (ipsectypes.h)
description: At what point IPsec has failed.
helpviewer_keywords: ["IPSEC_FAILURE_ME","IPSEC_FAILURE_NONE","IPSEC_FAILURE_PEER","IPSEC_FAILURE_POINT","IPSEC_FAILURE_POINT enumeration [Filtering]","IPSEC_FAILURE_POINT_MAX","fwp.ipsec_failure_point","ipsectypes/IPSEC_FAILURE_ME","ipsectypes/IPSEC_FAILURE_NONE","ipsectypes/IPSEC_FAILURE_PEER","ipsectypes/IPSEC_FAILURE_POINT","ipsectypes/IPSEC_FAILURE_POINT_MAX"]
old-location: fwp\ipsec_failure_point.htm
tech.root: fwp
ms.assetid: 750a5643-1157-4d15-9564-127756cd08cd
ms.date: 12/05/2018
ms.keywords: IPSEC_FAILURE_ME, IPSEC_FAILURE_NONE, IPSEC_FAILURE_PEER, IPSEC_FAILURE_POINT, IPSEC_FAILURE_POINT enumeration [Filtering], IPSEC_FAILURE_POINT_MAX, fwp.ipsec_failure_point, ipsectypes/IPSEC_FAILURE_ME, ipsectypes/IPSEC_FAILURE_NONE, ipsectypes/IPSEC_FAILURE_PEER, ipsectypes/IPSEC_FAILURE_POINT, ipsectypes/IPSEC_FAILURE_POINT_MAX
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: IPSEC_FAILURE_POINT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_FAILURE_POINT_
 - ipsectypes/IPSEC_FAILURE_POINT_
 - IPSEC_FAILURE_POINT
 - ipsectypes/IPSEC_FAILURE_POINT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_FAILURE_POINT
---

# IPSEC_FAILURE_POINT enumeration


## -description

The <b>IPSEC_FAILURE_POINT</b> enumerated type specifies at what point IPsec has failed.

## -enum-fields

### -field IPSEC_FAILURE_NONE:0

IPsec has not failed.

### -field IPSEC_FAILURE_ME

The local system is the failure point.

### -field IPSEC_FAILURE_PEER

A peer system is the failure point.

### -field IPSEC_FAILURE_POINT_MAX

Maximum value for testing only.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
