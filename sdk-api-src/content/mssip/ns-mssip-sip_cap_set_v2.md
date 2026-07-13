---
UID: NS:mssip._SIP_CAP_SET_V2
title: SIP_CAP_SET_V2 (mssip.h)
description: The SIP_CAP_SET_V2 structure defines the capabilities of a subject interface package (SIP). (SIP_CAP_SET_V2 structure)
helpviewer_keywords: ["*PSIP_CAP_SET_V2","PSIP_CAP_SET","PSIP_CAP_SET structure pointer [Security]","SIP_CAP_SET","SIP_CAP_SET structure [Security]","SIP_CAP_SET_V2","mssip/PSIP_CAP_SET","mssip/SIP_CAP_SET","security.sip_cap_set"]
old-location: security\sip_cap_set.htm
tech.root: security
ms.assetid: 0B6D173B-0183-4A7C-BB92-2D451F746164
ms.date: 08/02/2022
ms.keywords: '*PSIP_CAP_SET_V2, PSIP_CAP_SET, PSIP_CAP_SET structure pointer [Security], SIP_CAP_SET, SIP_CAP_SET structure [Security], SIP_CAP_SET_V2, mssip/PSIP_CAP_SET, mssip/SIP_CAP_SET, security.sip_cap_set'
req.header: mssip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: SIP_CAP_SET_V2, *PSIP_CAP_SET_V2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SIP_CAP_SET_V2
 - mssip/_SIP_CAP_SET_V2
 - PSIP_CAP_SET_V2
 - mssip/PSIP_CAP_SET_V2
 - SIP_CAP_SET_V2
 - mssip/SIP_CAP_SET_V2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mssip.h
api_name:
 - SIP_CAP_SET
---

# SIP_CAP_SET_V2 structure


## -description

The <b>SIP_CAP_SET</b> structure defines the capabilities of a <a href="/windows/desktop/SecGloss/s-gly">subject interface package</a> (SIP).

## -struct-fields

### -field cbSize

Size, in bytes, of this structure.

### -field dwVersion

The SIP version. By default, this value is two (2).

### -field isMultiSign

A value of one (1) indicates that the SIP supports multiple embedded signatures. Otherwise, set this value to zero (0).

### -field dwReserved

Reserved for future use. Set this value to zero (0).
