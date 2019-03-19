---
UID: NE:cfapi.CF_CALLBACK_CANCEL_FLAGS
title: CF_CALLBACK_CANCEL_FLAGS (cfapi.h)
author: windows-sdk-content
description: Callback flags for canceling data fetching for a placeholder file or folder.
old-location: cloudapi\cf_callback_cancel_flags.htm
tech.root: cfApi
ms.assetid: 16F0BB1E-FB9E-4AC3-8FD9-A540F72F1155
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CF_CALLBACK_CANCEL_FLAGS, CF_CALLBACK_CANCEL_FLAGS enumeration, CF_CALLBACK_CANCEL_FLAG_IO_ABORTED, CF_CALLBACK_CANCEL_FLAG_IO_TIMEOUT, CF_CALLBACK_CANCEL_FLAG_NONE, cfapi/CF_CALLBACK_CANCEL_FLAGS, cfapi/CF_CALLBACK_CANCEL_FLAG_IO_ABORTED, cfapi/CF_CALLBACK_CANCEL_FLAG_IO_TIMEOUT, cfapi/CF_CALLBACK_CANCEL_FLAG_NONE, cloudApi.cf_callback_cancel_flags
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
 - CF_CALLBACK_CANCEL_FLAGS
product: Windows
targetos: Windows
req.typenames: CF_CALLBACK_CANCEL_FLAGS
req.redist: 
---

# CF_CALLBACK_CANCEL_FLAGS enumeration


## -description


Callback flags for canceling data fetching for a placeholder file or folder.


## -enum-fields




### -field CF_CALLBACK_CANCEL_FLAG_NONE

No cancel flag.


### -field CF_CALLBACK_CANCEL_FLAG_IO_TIMEOUT

Flag to be set if the user request is cancelled as a result of the expiration of the 60 second timer.


### -field CF_CALLBACK_CANCEL_FLAG_IO_ABORTED

Flag to be set if the user request is cancelled as a result of the user explicitly terminating the hydration from app-initiated download toast.

