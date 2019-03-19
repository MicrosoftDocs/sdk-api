---
UID: NE:cfapi.CF_CALLBACK_FETCH_DATA_FLAGS
title: CF_CALLBACK_FETCH_DATA_FLAGS (cfapi.h)
author: windows-sdk-content
description: Callback flags for fetching data for a placeholder file or folder.
old-location: cloudapi\cf_callback_fetch_data_flags.htm
tech.root: cfApi
ms.assetid: 18C2CF8D-C59F-4181-953E-84B6BEC5F479
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CF_CALLBACK_FETCH_DATA_FLAGS, CF_CALLBACK_FETCH_DATA_FLAGS enumeration, CF_CALLBACK_FETCH_DATA_FLAG_EXPLICIT_HYDRATION, CF_CALLBACK_FETCH_DATA_FLAG_NONE, CF_CALLBACK_FETCH_DATA_FLAG_RECOVERY, cfapi/ CF_CALLBACK_FETCH_DATA_FLAG_EXPLICIT_HYDRATION, cfapi/CF_CALLBACK_FETCH_DATA_FLAGS, cfapi/CF_CALLBACK_FETCH_DATA_FLAG_NONE, cfapi/CF_CALLBACK_FETCH_DATA_FLAG_RECOVERY, cloudApi.cf_callback_fetch_data_flags
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_CALLBACK_FETCH_DATA_FLAGS
product: Windows
targetos: Windows
req.typenames: CF_CALLBACK_FETCH_DATA_FLAGS
req.redist: 
---

# CF_CALLBACK_FETCH_DATA_FLAGS enumeration


## -description


Callback flags for fetching data for a placeholder file or folder.


## -enum-fields




### -field CF_CALLBACK_FETCH_DATA_FLAG_NONE

No data fetch flag.


### -field CF_CALLBACK_FETCH_DATA_FLAG_RECOVERY

Flag to be used if the callback is invoked as a result of previously interrupted hydration process.


### -field CF_CALLBACK_FETCH_DATA_FLAG_EXPLICIT_HYDRATION

<b>Note</b>  This value is new for Windows 10, version 1803.

Flag to be used if the callback is invoked as a 
result of a call to <a href="https://msdn.microsoft.com/4FFD7580-BF59-48D0-B6D7-516559914096">CfHydratePlaceholder</a>. 


