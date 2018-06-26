---
UID: NE:cfapi.CF_CALLBACK_DEHYDRATE_FLAGS
title: CF_CALLBACK_DEHYDRATE_FLAGS
author: windows-sdk-content
description: Callback flags for notifying a sync provider that a placeholder under one of its sync root is going to be dehydrated.
old-location: cloudapi\cf_callback_dehydrate_flags.htm
old-project: cfApi
ms.assetid: DCB085EA-1468-44FB-9D45-F5C89693CBE7
ms.author: windowssdkdev
ms.date: 02/26/2018
ms.keywords: CF_CALLBACK_DEHYDRATE_FLAGS, CF_CALLBACK_DEHYDRATE_FLAGS enumeration, CF_CALLBACK_DEHYDRATE_FLAG_BACKGROUND, CF_CALLBACK_DEHYDRATE_FLAG_NONE, cfapi/CF_CALLBACK_DEHYDRATE_FLAGS, cfapi/CF_CALLBACK_DEHYDRATE_FLAG_BACKGROUND, cfapi/CF_CALLBACK_DEHYDRATE_FLAG_NONE, cloudApi.cf_callback_dehydrate_flags
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CF_CALLBACK_DEHYDRATE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_CALLBACK_DEHYDRATE_FLAGS
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# CF_CALLBACK_DEHYDRATE_FLAGS enumeration


## -description


Callback flags for notifying a sync provider that a placeholder under one of its sync root is going to be dehydrated.


## -enum-fields




### -field CF_CALLBACK_DEHYDRATE_FLAG_NONE

No dehydrate flag.


### -field CF_CALLBACK_DEHYDRATE_FLAG_BACKGROUND

A flag set if the dehydration request is initiated by a system background service.

