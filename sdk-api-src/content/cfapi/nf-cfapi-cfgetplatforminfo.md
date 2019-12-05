---
UID: NF:cfapi.CfGetPlatformInfo
title: CfGetPlatformInfo function (cfapi.h)
description: Gets the platform version information.
old-location: cloudapi\cfgetplatforminfo.htm
tech.root: cfApi
ms.assetid: BCF51702-87C1-405B-A3FF-98F5D0DDA8D5
ms.date: 12/05/2018
ms.keywords: CfGetPlatformInfo, CfGetPlatformInfo function, cfapi/CfGetPlatformInfo, cloudApi.cfgetplatforminfo
ms.topic: function
f1_keywords:
- cfapi/CfGetPlatformInfo
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- CldApi.dll
api_name:
- CfGetPlatformInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CfGetPlatformInfo function


## -description


Gets the platform version information.


## -parameters




### -param PlatformVersion [out]

The platform version information. See <a href="https://docs.microsoft.com/windows/desktop/api/cfapi/ns-cfapi-cf_platform_info">CF_PLATFORM_INFO</a> for more details.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



