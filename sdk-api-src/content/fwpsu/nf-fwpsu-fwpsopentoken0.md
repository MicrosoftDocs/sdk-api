---
UID: NF:fwpsu.FwpsOpenToken0
tech.root: fwp
title: FwpsOpenToken0
ms.date: 06/06/2024
targetos: Windows
description: Opens an access token.
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
 - FwpsOpenToken0
f1_keywords:
 - FwpsOpenToken0
 - fwpsu/FwpsOpenToken0
dev_langs:
 - c++
helpviewer_keywords:
 - FwpsOpenToken0
---

## -description

Opens an access token.

> [!NOTE]
> **FwpsOpenToken0** is a specific version of **FwpsOpenToken**. For more info, see [WFP version-independent names and targeting specific versions of Windows](/windows/win32/fwp/wfp-version-independent-names-and-targeting-specific-versions-of-windows).

## -parameters

### -param engineHandle

A handle for an open session to the filter engine. A callout driver calls the FwpmEngineOpen0 function to open a session to the filter engine.

### -param modifiedId

Specifies an LUID that changes each time the token is modified. An application can use this value as a test of whether a security context has changed since it was last used.

### -param desiredAccess

ACCESS_MASK structure specifying the requested types of access to the access token. These requested access types are compared with the token's discretionary access-control list (DACL) to determine which accesses are granted or denied.

### -param accessToken

Pointer to a caller-allocated variable that receives a handle to the newly opened access token.

## -returns

The **FwpsOpenToken0** function returns one of the following NTSTATUS codes.

|Return code|Description|
|-|-|
|STATUS_SUCCESS|The access token was successfully opened.|
|Other status codes|An error occurred.|

## -remarks

## -see-also
