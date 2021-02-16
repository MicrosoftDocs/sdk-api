---
UID: NS:winnt._SECURITY_CAPABILITIES
title: SECURITY_CAPABILITIES (winnt.h)
description: Defines the security capabilities of the app container.
helpviewer_keywords: ["*LPSECURITY_CAPABILITIES","*PSECURITY_CAPABILITIES","PSECURITY_CAPABILITIES","PSECURITY_CAPABILITIES structure pointer [Security]","SECURITY_CAPABILITIES","SECURITY_CAPABILITIES structure [Security]","_SECURITY_CAPABILITIES","security.security_capabilities","winnt/PSECURITY_CAPABILITIES","winnt/SECURITY_CAPABILITIES"]
old-location: security\security_capabilities.htm
tech.root: security
ms.assetid: 1A865519-E042-4871-886C-9AA64D71CCE4
ms.date: 12/05/2018
ms.keywords: '*LPSECURITY_CAPABILITIES, *PSECURITY_CAPABILITIES, PSECURITY_CAPABILITIES, PSECURITY_CAPABILITIES structure pointer [Security], SECURITY_CAPABILITIES, SECURITY_CAPABILITIES structure [Security], _SECURITY_CAPABILITIES, security.security_capabilities, winnt/PSECURITY_CAPABILITIES, winnt/SECURITY_CAPABILITIES'
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
req.typenames: SECURITY_CAPABILITIES, *PSECURITY_CAPABILITIES, *LPSECURITY_CAPABILITIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SECURITY_CAPABILITIES
 - winnt/_SECURITY_CAPABILITIES
 - PSECURITY_CAPABILITIES
 - winnt/PSECURITY_CAPABILITIES
 - SECURITY_CAPABILITIES
 - winnt/SECURITY_CAPABILITIES
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
 - SECURITY_CAPABILITIES
---

# SECURITY_CAPABILITIES structure


## -description

The <b>SECURITY_CAPABILITIES</b> structure defines the security capabilities of the app container.

## -struct-fields

### -field Capabilities.size_is

### -field Capabilities.size_is.CapabilityCount

### -field AppContainerSid

The SID of the app container.

### -field Capabilities

The specific capabilities.

### -field CapabilityCount

The number of the capabilities.

### -field Reserved

This member is reserved. Do not use it.

## -see-also

<a href="/windows/desktop/SecAuthZ/capability-sid-constants">Capability SID Constants</a>