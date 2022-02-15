---
UID: NE:opmapi._OPM_HDCP_PROTECTION_LEVEL
title: OPM_HDCP_PROTECTION_LEVEL (opmapi.h)
description: Specifies the protection level for High-Bandwidth Digital Content Protection (HDCP).
helpviewer_keywords: ["OPM_HDCP_FORCE_ULONG","OPM_HDCP_OFF","OPM_HDCP_ON","OPM_HDCP_PROTECTION_LEVEL","OPM_HDCP_PROTECTION_LEVEL enumeration [Media Foundation]","mf.opm_hdcp_protection_level","opmapi/OPM_HDCP_FORCE_ULONG","opmapi/OPM_HDCP_OFF","opmapi/OPM_HDCP_ON","opmapi/OPM_HDCP_PROTECTION_LEVEL"]
old-location: mf\opm_hdcp_protection_level.htm
tech.root: mf
ms.assetid: 698050e4-9726-49fa-85ed-9ae057e8c308
ms.date: 12/05/2018
ms.keywords: OPM_HDCP_FORCE_ULONG, OPM_HDCP_OFF, OPM_HDCP_ON, OPM_HDCP_PROTECTION_LEVEL, OPM_HDCP_PROTECTION_LEVEL enumeration [Media Foundation], mf.opm_hdcp_protection_level, opmapi/OPM_HDCP_FORCE_ULONG, opmapi/OPM_HDCP_OFF, opmapi/OPM_HDCP_ON, opmapi/OPM_HDCP_PROTECTION_LEVEL
req.header: opmapi.h
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
req.typenames: OPM_HDCP_PROTECTION_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_HDCP_PROTECTION_LEVEL
 - opmapi/_OPM_HDCP_PROTECTION_LEVEL
 - OPM_HDCP_PROTECTION_LEVEL
 - opmapi/OPM_HDCP_PROTECTION_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - opmapi.h
api_name:
 - OPM_HDCP_PROTECTION_LEVEL
---

# OPM_HDCP_PROTECTION_LEVEL enumeration


## -description

Specifies the protection level for High-Bandwidth Digital Content Protection (HDCP).

## -enum-fields

### -field OPM_HDCP_OFF:0

HDCP is disabled.

### -field OPM_HDCP_ON:1

HDCP is enabled.

### -field OPM_HDCP_FORCE_ULONG:0x7fffffff

Reserved.

## -remarks

This enumeration is numerically equivalent to the <b>COPP_HDCP_Protection_Level</b> enumeration used in Certified Output Protection Protocol (COPP).

## -see-also

<a href="/windows/desktop/medfound/opm-enumerations">OPM Enumerations</a>
