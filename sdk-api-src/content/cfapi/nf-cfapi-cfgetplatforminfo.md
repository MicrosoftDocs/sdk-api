---
UID: NF:cfapi.CfGetPlatformInfo
title: CfGetPlatformInfo function (cfapi.h)
description: Gets the platform version information.
helpviewer_keywords: ["CfGetPlatformInfo","CfGetPlatformInfo function","cfapi/CfGetPlatformInfo","cloudApi.cfgetplatforminfo"]
old-location: cloudapi\cfgetplatforminfo.htm
tech.root: cloudapi
ms.assetid: BCF51702-87C1-405B-A3FF-98F5D0DDA8D5
ms.date: 03/30/2023
ms.keywords: CfGetPlatformInfo, CfGetPlatformInfo function, cfapi/CfGetPlatformInfo, cloudApi.cfgetplatforminfo
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
 - CfGetPlatformInfo
 - cfapi/CfGetPlatformInfo
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
 - CfGetPlatformInfo
---

# CfGetPlatformInfo function

## -description

Gets version information for the cloud files platform.

## -parameters

### -param PlatformVersion [out]

The platform version information. See [CF_PLATFORM_INFO](ns-cfapi-cf_platform_info.md) for more details.

## -returns

If this function succeeds, it returns `S_OK`. Otherwise, it returns an **HRESULT** error code.

## -remarks

The *platform* is defined as the combination of the filter and the API library, which are always kept in sync with each other. This API is mainly intended for sync providers that run on multiple Windows versions and need to make decisions based on the platform capabilities. The platform version information consists of three parts: build number, revision number, and integration number. The build number and revision number change when the platform is serviced by Windows Update. The integration number on its own is indicative of the platform capability, both in terms of the API contracts and the availability of critical bug fixes. The integration number increments monotonically. The platform never loses capability with the increment of the integration number. Applications that are cloud files aware may also find this API useful.

## -see-also

[CF_PLATFORM_INFO](ns-cfapi-cf_platform_info.md)
