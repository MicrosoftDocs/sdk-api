---
UID: NF:fwpsu.FwpsAleEndpointSetSecurityInfo0
tech.root: fwp
title: FwpsAleEndpointSetSecurityInfo0
ms.date: 06/06/2024
targetos: Windows
description: Sets security information about the application layer enforcement (ALE) endpoint enumeration session.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: fwpsu.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: fwpuclnt.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fwpsu.h
api_name:
 - FwpsAleEndpointSetSecurityInfo0
f1_keywords:
 - FwpsAleEndpointSetSecurityInfo0
 - fwpsu/FwpsAleEndpointSetSecurityInfo0
dev_langs:
 - c++
helpviewer_keywords:
 - FwpsAleEndpointSetSecurityInfo0
---

## -description

Sets security information about the application layer enforcement (ALE) endpoint enumeration session.

> [!NOTE]
> **FwpsAleEndpointSetSecurityInfo0** is a specific version of **FwpsAleEndpointSetSecurityInfo**. For more info, see [WFP version-independent names and targeting specific versions of Windows](/windows/win32/fwp/wfp-version-independent-names-and-targeting-specific-versions-of-windows).

## -parameters

### -param engineHandle

A handle for an open session with the filter engine. This handle is obtained when a session is opened by calling **FwpmEngineOpen0**.

### -param securityInfo

A set of security information flags. For more information, see the **SECURITY_INFORMATION** description in the Installable File Systems driver documentation.

### -param sidOwner

The security identifier of the security owner.

### -param sidGroup

The security identifier of the security group.

### -param dacl

The discretionary access control list.

### -param sacl

The system access control list.

## -returns

## -remarks

## -see-also
