---
UID: NE:cfapi.CF_CONNECT_FLAGS
title: CF_CONNECT_FLAGS
author: windows-driver-content
description: Additional information that can be requested by a sync provider when its callbacks are invoked.
old-location: cloudapi\cf_connect_flags.htm
old-project: cfApi
ms.assetid: C1CAC75C-9CB6-4172-A437-AE366D99DA9F
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CF_CONNECT_FLAGS, CF_CONNECT_FLAGS enumeration, CF_CONNECT_FLAG_BLOCK_SELF_IMPLICIT_HYDRATION, CF_CONNECT_FLAG_NONE, CF_CONNECT_FLAG_REQUIRE_FULL_FILE_PATH, CF_CONNECT_FLAG_REQUIRE_PROCESS_INFO, cfapi/ CF_CONNECT_FLAG_BLOCK_SELF_IMPLICIT_HYDRATION, cfapi/CF_CONNECT_FLAGS, cfapi/CF_CONNECT_FLAG_NONE, cfapi/CF_CONNECT_FLAG_REQUIRE_FULL_FILE_PATH, cfapi/CF_CONNECT_FLAG_REQUIRE_PROCESS_INFO, cloudApi.cf_connect_flags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: CF_CONNECT_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CfApi.h
api_name:
-	CF_CONNECT_FLAGS
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# CF_CONNECT_FLAGS enumeration


## -description


Additional information that can be requested by a sync provider when its callbacks are invoked.


## -enum-fields




### -field CF_CONNECT_FLAG_NONE

No connection flags.


### -field CF_CONNECT_FLAG_REQUIRE_PROCESS_INFO

When this flag is specified, the platform returns the full image path of the hydrating process in the callback parameters.


### -field CF_CONNECT_FLAG_REQUIRE_FULL_FILE_PATH

When this flag is specified, the platform returns the full path of the placeholder being requested in the callback parameters.


#### - CF_CONNECT_FLAG_BLOCK_SELF_IMPLICIT_HYDRATION

<b>Note</b>  This value is new for Windows 10, version 1803.

When this flag is specified, The implicit hydration, which is not performed via <a href="https://msdn.microsoft.com/4FFD7580-BF59-48D0-B6D7-516559914096">CfHydratePlaceholder</a>, can happen when the anti-virus software scans a sync provider’s file system activities on non-hydrated cloud file placeholders. This kind of implicit hydration is not expected. If the sync provider never initiates implicit hydration operations, it can instruct the platform to block all such implicit hydration operations, as opposed to failing the <b>FETCH_DATA</b> callbacks later.  


