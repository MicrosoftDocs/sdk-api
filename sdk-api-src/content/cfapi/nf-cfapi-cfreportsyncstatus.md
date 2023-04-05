---
UID: NF:cfapi.CfReportSyncStatus
title: CfReportSyncStatus function (cfapi.h)
description: Allows a sync provider to notify the platform of its status on a specified sync root without having to connect with a call to CfConnectSyncRoot first.
helpviewer_keywords: ["CfReportSyncStatus","CfReportSyncStatus function","cfapi/CfReportSyncStatus","cloudApi.cfreportsyncstatus"]
old-location: cloudapi\cfreportsyncstatus.htm
tech.root: cloudapi
ms.assetid: DC77D18A-CBF4-4172-815A-AB49A48D10B3
ms.date: 03/30/2023
ms.keywords: CfReportSyncStatus, CfReportSyncStatus function, cfapi/CfReportSyncStatus, cloudApi.cfreportsyncstatus
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
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
 - CfReportSyncStatus
 - cfapi/CfReportSyncStatus
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
 - CfReportSyncStatus
---

# CfReportSyncStatus function

## -description

Allows a sync provider to notify the platform of its status on a specified sync root without having to connect with a call to [CfConnectSyncRoot](nf-cfapi-cfconnectsyncroot.md) first.

## -parameters

### -param SyncRootPath [in, out]

Path to the sync root.

### -param SyncStatus [in]

The sync status to report; if `NULL`, clears the previously-saved sync status. For more information, see the [Remarks](#-remarks) section, below.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

When a non-null [CF_SYNC_STATUS](ns-cfapi-cf_sync_status.md) is provided in the *SyncStatus* parameter, the information will be remembered on the sync root until it is cleared explicitly by the sync provider or when the machine reboots. The platform will query this information upon any failed operations on a cloud file placeholder, using the following process:

1. The platform will first search for sync status at the file level.
2. If no sync status is found, the platform will then search for sync status registered at the sync root level, which is done through this function.
3. Once a sync status is located, the platform will use the information provided to construct a more meaningful and actionable message to the user.

**CfReportSyncStatus** clears the previously-saved sync status when being called with a `NULL` sync status. No change will be made to the existing sync status if the function call fails.

## -see-also

[CfConnectSyncRoot](nf-cfapi-cfconnectsyncroot.md)

[CF_SYNC_STATUS](ns-cfapi-cf_sync_status.md)
