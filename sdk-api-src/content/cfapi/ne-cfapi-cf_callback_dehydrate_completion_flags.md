---
UID: NE:cfapi.CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
title: CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
author: windows-sdk-content
description: A callback flag to inform the sync provider that a placeholder under one of its sync roots has been successfully dehydrated.
old-location: cloudapi\cf_callback_dehydrate_completion_flags.htm
old-project: cfApi
ms.assetid: BB39BC4D-A5FF-4204-A7ED-30605B865F15
ms.author: windowssdkdev
ms.date: 02/27/2018
ms.keywords: CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS, CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS enumeration, CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_BACKGROUND, CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_DEHYDRATED, CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_NONE, cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS, cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_BACKGROUND, cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_DEHYDRATED, cfapi/CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_NONE, cloudApi.cf_callback_dehydrate_completion_flags
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
req.typenames: CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# CF_CALLBACK_DEHYDRATE_COMPLETION_FLAGS enumeration


## -description


A callback flag to inform the sync provider that a placeholder under one of its sync roots has been successfully dehydrated.


## -enum-fields




### -field CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_NONE

No dehydration completion flag.


### -field CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_BACKGROUND

A flag set if the dehydration request is initiated by a system background service.


### -field CF_CALLBACK_DEHYDRATE_COMPLETION_FLAG_DEHYDRATED

A flag set if the placeholder was hydrated prior to the dehydration request.

