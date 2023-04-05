---
UID: NE:cfapi.CF_SYNC_ROOT_INFO_CLASS
title: CF_SYNC_ROOT_INFO_CLASS (cfapi.h)
description: Types of sync root information.
helpviewer_keywords: ["CF_SYNC_ROOT_INFO_BASIC","CF_SYNC_ROOT_INFO_CLASS","CF_SYNC_ROOT_INFO_CLASS enumeration","CF_SYNC_ROOT_INFO_PROVIDER","CF_SYNC_ROOT_INFO_STANDARD","cfapi/CF_SYNC_ROOT_INFO_BASIC","cfapi/CF_SYNC_ROOT_INFO_CLASS","cfapi/CF_SYNC_ROOT_INFO_PROVIDER","cfapi/CF_SYNC_ROOT_INFO_STANDARD","cloudApi.cf_sync_root_info_class"]
old-location: cloudapi\cf_sync_root_info_class.htm
tech.root: cloudapi
ms.assetid: 4415E075-048E-4B9F-B293-5F7A63CAE3A4
ms.date: 03/29/2023
ms.keywords: CF_SYNC_ROOT_INFO_BASIC, CF_SYNC_ROOT_INFO_CLASS, CF_SYNC_ROOT_INFO_CLASS enumeration, CF_SYNC_ROOT_INFO_PROVIDER, CF_SYNC_ROOT_INFO_STANDARD, cfapi/CF_SYNC_ROOT_INFO_BASIC, cfapi/CF_SYNC_ROOT_INFO_CLASS, cfapi/CF_SYNC_ROOT_INFO_PROVIDER, cfapi/CF_SYNC_ROOT_INFO_STANDARD, cloudApi.cf_sync_root_info_class
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CF_SYNC_ROOT_INFO_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_SYNC_ROOT_INFO_CLASS
 - cfapi/CF_SYNC_ROOT_INFO_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_SYNC_ROOT_INFO_CLASS
---

# CF_SYNC_ROOT_INFO_CLASS enumeration

## -description

Types of sync root information.

## -enum-fields

### -field CF_SYNC_ROOT_INFO_BASIC:0

Basic sync root information is provided. See [CF_SYNC_ROOT_BASIC_INFO](ns-cfapi-cf_sync_root_basic_info.md).

### -field CF_SYNC_ROOT_INFO_STANDARD:1

Standard sync root information is provided. See [CF_SYNC_ROOT_STANDARD_INFO](ns-cfapi-cf_sync_root_standard_info.md).

### -field CF_SYNC_ROOT_INFO_PROVIDER:2

Sync root provider information is being provided. See [CF_SYNC_ROOT_PROVIDER_INFO](ns-cfapi-cf_sync_root_provider_info.md).

## -see-also

[CfGetSyncRootInfoByPath](nf-cfapi-cfgetsyncrootinfobypath.md)

[CF_SYNC_ROOT_BASIC_INFO](ns-cfapi-cf_sync_root_basic_info.md)

[CF_SYNC_ROOT_STANDARD_INFO](ns-cfapi-cf_sync_root_standard_info.md)

[CF_SYNC_ROOT_PROVIDER_INFO](ns-cfapi-cf_sync_root_provider_info.md)
