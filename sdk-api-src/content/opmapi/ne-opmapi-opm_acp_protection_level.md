---
UID: NE:opmapi._OPM_ACP_PROTECTION_LEVEL
title: OPM_ACP_PROTECTION_LEVEL (opmapi.h)
description: Specifies the protection level for Analog Copy Protection (ACP).
helpviewer_keywords: ["OPM_ACP_FORCE_ULONG","OPM_ACP_LEVEL_ONE","OPM_ACP_LEVEL_THREE","OPM_ACP_LEVEL_TWO","OPM_ACP_OFF","OPM_ACP_PROTECTION_LEVEL","OPM_ACP_PROTECTION_LEVEL enumeration [Media Foundation]","mf.opm_acp_protection_level","opmapi/OPM_ACP_FORCE_ULONG","opmapi/OPM_ACP_LEVEL_ONE","opmapi/OPM_ACP_LEVEL_THREE","opmapi/OPM_ACP_LEVEL_TWO","opmapi/OPM_ACP_OFF","opmapi/OPM_ACP_PROTECTION_LEVEL"]
old-location: mf\opm_acp_protection_level.htm
tech.root: mf
ms.assetid: f52b4ee6-1ab3-4153-86e3-5ae69fd8a958
ms.date: 12/05/2018
ms.keywords: OPM_ACP_FORCE_ULONG, OPM_ACP_LEVEL_ONE, OPM_ACP_LEVEL_THREE, OPM_ACP_LEVEL_TWO, OPM_ACP_OFF, OPM_ACP_PROTECTION_LEVEL, OPM_ACP_PROTECTION_LEVEL enumeration [Media Foundation], mf.opm_acp_protection_level, opmapi/OPM_ACP_FORCE_ULONG, opmapi/OPM_ACP_LEVEL_ONE, opmapi/OPM_ACP_LEVEL_THREE, opmapi/OPM_ACP_LEVEL_TWO, opmapi/OPM_ACP_OFF, opmapi/OPM_ACP_PROTECTION_LEVEL
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
req.typenames: OPM_ACP_PROTECTION_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_ACP_PROTECTION_LEVEL
 - opmapi/_OPM_ACP_PROTECTION_LEVEL
 - OPM_ACP_PROTECTION_LEVEL
 - opmapi/OPM_ACP_PROTECTION_LEVEL
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
 - OPM_ACP_PROTECTION_LEVEL
---

# OPM_ACP_PROTECTION_LEVEL enumeration


## -description

Specifies the protection level for Analog Copy Protection (ACP).

## -enum-fields

### -field OPM_ACP_OFF:0

ACP is disabled.

### -field OPM_ACP_LEVEL_ONE:1

ACP protection level 1.

### -field OPM_ACP_LEVEL_TWO:2

ACP protection level 2.

### -field OPM_ACP_LEVEL_THREE:3

ACP protection level 3.

### -field OPM_ACP_FORCE_ULONG:0x7fffffff

Reserved.

## -remarks

This enumeration is numerically equivalent to the <b>COPP_ACP_Protection_Level</b> enumeration used in Certified Output Protection Protocol. The OPM_ACP_OFF flag corresponds to COPP_ACP_Level0.

## -see-also

<a href="/windows/desktop/medfound/opm-enumerations">OPM Enumerations</a>
