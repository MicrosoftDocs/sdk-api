---
UID: NF:cfapi.CfConnectSyncRoot
title: CfConnectSyncRoot function (cfapi.h)
description: Initiates bi-directional communication between a sync provider and the sync filter API.
helpviewer_keywords: ["CfConnectSyncRoot","CfConnectSyncRoot function","cfapi/CfConnectSyncRoot","cloudApi.cfconnectsyncroot"]
old-location: cloudapi\cfconnectsyncroot.htm
tech.root: cloudapi
ms.assetid: 287DA978-9797-48DF-9C90-BA53BB82475C
ms.date: 03/30/2023
ms.keywords: CfConnectSyncRoot, CfConnectSyncRoot function, cfapi/CfConnectSyncRoot, cloudApi.cfconnectsyncroot
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfConnectSyncRoot
 - cfapi/CfConnectSyncRoot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfConnectSyncRoot
---

# CfConnectSyncRoot function

## -description

Initiates bi-directional communication between a sync provider and the sync filter API.

## -parameters

### -param SyncRootPath [in]

The path to the sync root.

### -param CallbackTable [in]

The callback table to be registered. This parameter is how the sync provider tells the library which functions to call for various types of requests from the platform. It is an array of structures containing a callback type and associated function pointer. The sync provider only needs to register the callbacks it implements. The *CallbackTable* array should always end with **CF_CALLBACK_REGISTRATION_END**.

### -param CallbackContext [in, optional]

*CallbackContext* is provided for the convenience of the sync provider. The platform will remember this *CallbackContext* and pass it back to the sync provider any time one of its callback functions is invoked on the current sync root. A good use for the *CallbackContext* would be a pointer into the sync provider’s own structure that maintains state for this connection.

### -param ConnectFlags [in]

The sync provider can request additional information be provided when its callbacks are invoked by passing *ConnectFlags* to this API. The following flags are supported:

| Request | Description |
|--------|--------|
| **REQUEST_PROCESS_INFO** | The platform returns the full image path of the hydrating process in the callback parameters when this flag is specified. |
| **REQUIRE_FULL_FILE_PATH** | The platform returns the full path of the placeholder being requested in the callback parameters when this flag is specified. |
| **BLOCK_SELF_IMPLICIT_HYDRATION** | The implicit hydration, which is not performed via [CfHydratePlaceholder](nf-cfapi-cfhydrateplaceholder.md), can happen when Anti-Virus software scans sync provider’s file system activities on non-hydrated cloud file placeholders. This kind of implicit hydrations is not expected. If the sync provider never initiates implicit hydration operations itself, it can instruct the platform block all such implicit hydration operations as opposed to failing the **FETCH_DATA** callbacks later. |

### -param ConnectionKey [out]

On successful return, this API will return an opaque *ConnectionKey* back to the sync provider. This represents the communication channel that was just established, and the sync provider may remember the *ConnectionKey* and pass it when calling various sync provider APIs. If a sync provider only expects to establish a single connection, then the *ConnectionKey* could be stored in a global. However, the platform supports a single provider process connecting to multiple different sync roots at the same time, and for each connection there will be a different *ConnectionKey* returned. A good place to store each *ConnectionKey* would be inside the sync provider’s internal structure identified by the *CallbackContext*.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

This initiates a bi-directional communication channel between the sync provider and the sync filter. A sync provider typically calls this API soon after startup, once it has been initialized and is ready to service requests.

The sync root must be registered with the platform prior to being connected. For a given *SyncRootPath*, there can be at most one connection established at any given time.

 The sync provider should have **WRITE_DATA** or **WRITE_DAC** access to the sync root to be connected or the API will be failed with **HRESULT(ERROR_CLOUD_FILE_ACCESS_DENIED)**.

## -see-also

[CfHydratePlaceholder](nf-cfapi-cfhydrateplaceholder.md)
