---
UID: NS:winnt._CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE
title: CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE (winnt.h)
description: Specifies the OCTET_STRING value type of the claim security attribute.
helpviewer_keywords: ["*PCLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE","CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE","CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE structure [Security]","PCLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE","PCLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE structure pointer [Security]","_CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE","security.claim_security_attribute_octet_string_value","winnt/CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE","winnt/PCLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE"]
old-location: security\claim_security_attribute_octet_string_value.htm
tech.root: security
ms.assetid: 6647CC4F-1A84-43B2-A80E-7B6BF3A2D7AD
ms.date: 12/05/2018
ms.keywords: '*PCLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE, CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE, CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE structure [Security], PCLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE, PCLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE structure pointer [Security], _CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE, security.claim_security_attribute_octet_string_value, winnt/CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE, winnt/PCLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE'
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
req.typenames: CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE, *PCLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE
 - winnt/_CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE
 - PCLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE
 - winnt/PCLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE
 - CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE
 - winnt/CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE
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
 - CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE
---

# CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE structure


## -description

The 	<b>CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE</b> structure specifies  the <b>OCTET_STRING</b> value type of the claim security attribute.

## -struct-fields

### -field pValue

A pointer buffer that contains the <b>OCTET_STRING</b> value. The value is a series of bytes of the length indicated in the <b>ValueLength</b>  member.

### -field ValueLength

The length, in bytes, of the <b>OCTET_STRING</b>  value.

