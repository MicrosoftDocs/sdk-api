---
UID: NF:cfapi.CfGetPlatformInfo
title: CfGetPlatformInfo function
author: windows-driver-content
description: Gets the platform version information.
old-location: cloudapi\cfgetplatforminfo.htm
old-project: cfApi
ms.assetid: BCF51702-87C1-405B-A3FF-98F5D0DDA8D5
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CfGetPlatformInfo, CfGetPlatformInfo function, cfapi/CfGetPlatformInfo, cloudApi.cfgetplatforminfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: CF_PLACEHOLDER_RANGE_INFO_CLASS, *PCF_PLACEHOLDER_RANGE_INFO_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	CldApi.dll
api_name:
-	CfGetPlatformInfo
product: Windows
targetos: Windows
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
---

# CfGetPlatformInfo function


## -description


Gets the platform version information.


## -parameters




### -param PlatformVersion [out]

The platform version information. See <a href="https://msdn.microsoft.com/BEB1CBF0-05FB-4D48-AC43-AA957F2208DB">CF_PLATFORM_INFO</a> for more details.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



