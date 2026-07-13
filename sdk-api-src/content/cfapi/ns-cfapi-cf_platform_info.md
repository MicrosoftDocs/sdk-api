---
UID: NS:cfapi.CF_PLATFORM_INFO
title: CF_PLATFORM_INFO (cfapi.h)
description: Returns information for the cloud files platform. This is intended for sync providers running on multiple versions of Windows.
helpviewer_keywords: ["CF_PLATFORM_INFO","CF_PLATFORM_INFO structure","cfapi/CF_PLATFORM_INFO","cloudApi.cf_platform_info"]
old-location: cloudapi\cf_platform_info.htm
tech.root: cloudapi
ms.assetid: BEB1CBF0-05FB-4D48-AC43-AA957F2208DB
ms.date: 04/04/2023
ms.keywords: CF_PLATFORM_INFO, CF_PLATFORM_INFO structure, cfapi/CF_PLATFORM_INFO, cloudApi.cf_platform_info
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
req.typenames: CF_PLATFORM_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_PLATFORM_INFO
 - cfapi/CF_PLATFORM_INFO
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
 - CF_PLATFORM_INFO
---

# CF_PLATFORM_INFO structure

## -description

Returns information for the cloud files platform. This is intended for sync providers running on multiple versions of Windows.

## -struct-fields

### -field BuildNumber

The build number of the Windows platform version. Changes when the platform is serviced by a Windows update.

### -field RevisionNumber

The revision number of the Windows platform version. Changes when the platform is serviced by a Windows update.

### -field IntegrationNumber

The integration number of the Windows platform version. This is indicative of the platform capabilities, both in terms of API contracts and availability of bug fixes.

## -remarks

The platform is a combination of the cloud filter and the placeholder files API library, which are always kept in sync with each other. This API is intended for sync providers that need to make decisions based on the platform capabilities of multiple versions of Windows.

If you are building an app that uses or is aware of placeholder files, this may be useful to you.

## -see-also

[CfGetPlatformInfo](nf-cfapi-cfgetplatforminfo.md)
