---
UID: NS:cfapi.CF_SYNC_ROOT_STANDARD_INFO
title: CF_SYNC_ROOT_STANDARD_INFO
author: windows-sdk-content
description: Standard sync root information.
old-location: cloudapi\cf_sync_root_standard_info.htm
old-project: cfApi
ms.assetid: 17E409FB-2997-432C-977F-BEBF53068B42
ms.author: windowssdkdev
ms.date: 02/27/2018
ms.keywords: CF_SYNC_ROOT_STANDARD_INFO, CF_SYNC_ROOT_STANDARD_INFO structure, cfapi/CF_SYNC_ROOT_STANDARD_INFO, cloudApi.cf_sync_root_standard_info
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: CF_SYNC_ROOT_STANDARD_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_SYNC_ROOT_STANDARD_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CF_SYNC_ROOT_STANDARD_INFO structure


## -description


Standard sync root information.


## -struct-fields




### -field SyncRootFileId

File ID of the sync root.


### -field HydrationPolicy

Hydration policy of the sync root.


### -field PopulationPolicy

Population policy of the sync root.


### -field InSyncPolicy

In-sync policy of the sync root.


### -field HardLinkPolicy

Sync root hard linking policy.


### -field ProviderStatus

Status of the sync root provider.


### -field ProviderName

 


### -field ProviderVersion

 


### -field SyncRootIdentityLength

Length, in bytes, of the <i>SyncRootIdentity</i>.


### -field SyncRootIdentity

 




#### - ProviderName[CF_MAX_PROVIDER_NAME_LENGTH + 1]

Name of the sync root.


#### - ProviderVersion[CF_MAX_PROVIDER_VERSION_LENGTH + 1]

Version of the sync root.


#### - SyncRootIdentity[1]

The identity of the sync root directory.


## -remarks



<b>CF_MAX_PROVIDER_NAME_LENGTH</b> and <b>CF_MAX_PROVIDER_VERSION_LENGTH</b>  are set to 255.



