---
UID: NS:cfapi.CF_SYNC_ROOT_PROVIDER_INFO
title: CF_SYNC_ROOT_PROVIDER_INFO
author: windows-sdk-content
description: Sync root provider information.
old-location: cloudapi\cf_sync_root_provider_info.htm
old-project: cfApi
ms.assetid: 9EBC64B5-7FB3-41AA-BCB2-29B3E444B463
ms.author: windowssdkdev
ms.date: 02/26/2018
ms.keywords: CF_SYNC_ROOT_PROVIDER_INFO, CF_SYNC_ROOT_PROVIDER_INFO structure, cfapi/CF_SYNC_ROOT_PROVIDER_INFO, cloudApi.cf_sync_root_provider_info
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
req.typenames: CF_SYNC_ROOT_PROVIDER_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_SYNC_ROOT_PROVIDER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# CF_SYNC_ROOT_PROVIDER_INFO structure


## -description


Sync root provider information.


## -struct-fields




### -field ProviderStatus

Status of the sync root provider.


### -field ProviderName

 


### -field ProviderVersion

 




#### - ProviderName[CF_MAX_PROVIDER_NAME_LENGTH + 1]

Name of the sync root provider.


#### - ProviderVersion[CF_MAX_PROVIDER_VERSION_LENGTH + 1]

Version of the sync root provider.


## -remarks



<b>CF_MAX_PROVIDER_NAME_LENGTH</b> and <b>CF_MAX_PROVIDER_VERSION_LENGTH</b>  are set to 255.



