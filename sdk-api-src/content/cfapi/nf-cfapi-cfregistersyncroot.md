---
UID: NF:cfapi.CfRegisterSyncRoot
title: CfRegisterSyncRoot function (cfapi.h)
description: Performs a one time sync root registration.
helpviewer_keywords: ["CfRegisterSyncRoot","CfRegisterSyncRoot function","cfapi/CfRegisterSyncRoot","cloudApi.cfregistersyncroot"]
old-location: cloudapi\cfregistersyncroot.htm
tech.root: cloudapi
ms.assetid: FAD56873-8812-42DC-9975-9507F73BD9E3
ms.date: 12/05/2018
ms.keywords: CfRegisterSyncRoot, CfRegisterSyncRoot function, cfapi/CfRegisterSyncRoot, cloudApi.cfregistersyncroot
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
 - CfRegisterSyncRoot
 - cfapi/CfRegisterSyncRoot
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
 - CfRegisterSyncRoot
---

# CfRegisterSyncRoot function


## -description

Performs a one time  sync root registration.

## -parameters

### -param SyncRootPath [in]

The path to the sync root to be registered.

### -param Registration [in]

Contains information about the sync provider and sync root to be registered.

### -param Policies [in]

The policies of the sync root to be registered.

### -param RegisterFlags [in]

Flags for registering previous and new sync roots.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This can be used at a sync provider install time, first time set up for an individual user, or when a user configures another sync root (if this scenario is supported). 

This performs a one time sync root registration, which allows a sync provider to utilize an entire directory tree structure.  Note that no two sync roots  directory trees can overlap with one another.

