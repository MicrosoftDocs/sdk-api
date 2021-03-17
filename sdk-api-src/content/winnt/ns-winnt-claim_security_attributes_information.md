---
UID: NS:winnt._CLAIM_SECURITY_ATTRIBUTES_INFORMATION
title: CLAIM_SECURITY_ATTRIBUTES_INFORMATION (winnt.h)
description: Defines the security attributes for the claim.
helpviewer_keywords: ["*PCLAIM_SECURITY_ATTRIBUTES_INFORMATION","CLAIM_SECURITY_ATTRIBUTES_INFORMATION","CLAIM_SECURITY_ATTRIBUTES_INFORMATION structure [Security]","PCLAIM_SECURITY_ATTRIBUTES_INFORMATION","PCLAIM_SECURITY_ATTRIBUTES_INFORMATION structure pointer [Security]","_CLAIM_SECURITY_ATTRIBUTES_INFORMATION","security.claim_security_attributes_information","winnt/CLAIM_SECURITY_ATTRIBUTES_INFORMATION","winnt/PCLAIM_SECURITY_ATTRIBUTES_INFORMATION"]
old-location: security\claim_security_attributes_information.htm
tech.root: security
ms.assetid: D7D9816E-1ECE-48CA-9F2F-0955572A0FCA
ms.date: 12/05/2018
ms.keywords: '*PCLAIM_SECURITY_ATTRIBUTES_INFORMATION, CLAIM_SECURITY_ATTRIBUTES_INFORMATION, CLAIM_SECURITY_ATTRIBUTES_INFORMATION structure [Security], PCLAIM_SECURITY_ATTRIBUTES_INFORMATION, PCLAIM_SECURITY_ATTRIBUTES_INFORMATION structure pointer [Security], _CLAIM_SECURITY_ATTRIBUTES_INFORMATION, security.claim_security_attributes_information, winnt/CLAIM_SECURITY_ATTRIBUTES_INFORMATION, winnt/PCLAIM_SECURITY_ATTRIBUTES_INFORMATION'
req.header: winnt.h
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
req.typenames: CLAIM_SECURITY_ATTRIBUTES_INFORMATION, *PCLAIM_SECURITY_ATTRIBUTES_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLAIM_SECURITY_ATTRIBUTES_INFORMATION
 - winnt/_CLAIM_SECURITY_ATTRIBUTES_INFORMATION
 - PCLAIM_SECURITY_ATTRIBUTES_INFORMATION
 - winnt/PCLAIM_SECURITY_ATTRIBUTES_INFORMATION
 - CLAIM_SECURITY_ATTRIBUTES_INFORMATION
 - winnt/CLAIM_SECURITY_ATTRIBUTES_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - CLAIM_SECURITY_ATTRIBUTES_INFORMATION
---

# CLAIM_SECURITY_ATTRIBUTES_INFORMATION structure


## -description

The <b>CLAIM_SECURITY_ATTRIBUTES_INFORMATION</b> structure defines the security attributes for the claim.

## -struct-fields

### -field Version

The version of the security attribute. This must be CLAIM_SECURITY_ATTRIBUTES_INFORMATION_VERSION_V1.

### -field Reserved

This member is currently reserved and must be zero when setting an attribute and is ignored when getting an attribute.

### -field AttributeCount

The number of values.

### -field Attribute

The actual attribute.

### -field Attribute.pAttributeV1

Pointer to an array that contains the <b>AttributeCount</b> member of the <a href="/windows/desktop/api/winnt/ns-winnt-claim_security_attribute_v1">CLAIM_SECURITY_ATTRIBUTE_V1</a> structure.