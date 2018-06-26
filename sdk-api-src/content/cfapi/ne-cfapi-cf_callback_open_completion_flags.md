---
UID: NE:cfapi.CF_CALLBACK_OPEN_COMPLETION_FLAGS
title: CF_CALLBACK_OPEN_COMPLETION_FLAGS
author: windows-sdk-content
description: Callback flags for notifying a sync provider that a placeholder was successfully opened for read/write/delete access.
old-location: cloudapi\cf_callback_open_completion_flags.htm
old-project: cfApi
ms.assetid: FF7EA010-B90A-46F8-A373-5C128B31FE70
ms.author: windowssdkdev
ms.date: 02/26/2018
ms.keywords: CF_CALLBACK_OPEN_COMPLETION_FLAGS, CF_CALLBACK_OPEN_COMPLETION_FLAGS enumeration, CF_CALLBACK_OPEN_COMPLETION_FLAG_NONE, CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNKNOWN, CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNSUPPORTED, cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAGS, cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAG_NONE, cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNKNOWN, cfapi/CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNSUPPORTED, cloudApi.cf_callback_open_completion_flags
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
req.typenames: CF_CALLBACK_OPEN_COMPLETION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_CALLBACK_OPEN_COMPLETION_FLAGS
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
---

# CF_CALLBACK_OPEN_COMPLETION_FLAGS enumeration


## -description


Callback flags for notifying a sync provider that a placeholder was successfully opened for read/write/delete access.


## -enum-fields




### -field CF_CALLBACK_OPEN_COMPLETION_FLAG_NONE

No open completion flag.


### -field CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNKNOWN

A flag set if the placeholder metadata is corrupted.


### -field CF_CALLBACK_OPEN_COMPLETION_FLAG_PLACEHOLDER_UNSUPPORTED

A flag set if the placeholder metadata is not supported.

