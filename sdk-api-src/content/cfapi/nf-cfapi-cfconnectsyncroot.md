---
UID: NF:cfapi.CfConnectSyncRoot
title: CfConnectSyncRoot function (cfapi.h)
description: Initiates bi-directional communication between a sync provider and the sync filter API.
helpviewer_keywords: ["CfConnectSyncRoot","CfConnectSyncRoot function","cfapi/CfConnectSyncRoot","cloudApi.cfconnectsyncroot"]
old-location: cloudapi\cfconnectsyncroot.htm
tech.root: cloudapi
ms.assetid: 287DA978-9797-48DF-9C90-BA53BB82475C
ms.date: 12/05/2018
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

The callback table to be registered.

### -param CallbackContext [in, optional]

A callback context used by the platform anytime a specified callback function is invoked.

### -param ConnectFlags [in]

Provides additional information when a callback is invoked.

### -param ConnectionKey [out]

A connection key representing the communication channel with the sync filter.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This initiates a bi-directional communication channel between the sync provider and the sync filter. A sync provider typically calls this API soon after startup, once it has been initialized and is ready to service requests.

The sync root must be registered prior to being connected. For a given <i>SyncRootPath</i>, there can be at most one connection established at any given time.

 The sync provider should have WRITE_DATA or WRITE_DAC access to the sync root to be connected or the API will be failed with HRESULT(ERROR_CLOUD_FILE_ACCESS_DENIED).

