---
UID: NE:cfapi.CF_CALLBACK_CANCEL_FLAGS
title: CF_CALLBACK_CANCEL_FLAGS (cfapi.h)
description: Callback flags for canceling data fetching for a placeholder file or folder.
helpviewer_keywords: ["CF_CALLBACK_CANCEL_FLAGS","CF_CALLBACK_CANCEL_FLAGS enumeration","CF_CALLBACK_CANCEL_FLAG_IO_ABORTED","CF_CALLBACK_CANCEL_FLAG_IO_TIMEOUT","CF_CALLBACK_CANCEL_FLAG_NONE","cfapi/CF_CALLBACK_CANCEL_FLAGS","cfapi/CF_CALLBACK_CANCEL_FLAG_IO_ABORTED","cfapi/CF_CALLBACK_CANCEL_FLAG_IO_TIMEOUT","cfapi/CF_CALLBACK_CANCEL_FLAG_NONE","cloudApi.cf_callback_cancel_flags"]
old-location: cloudapi\cf_callback_cancel_flags.htm
tech.root: cloudapi
ms.assetid: 16F0BB1E-FB9E-4AC3-8FD9-A540F72F1155
ms.date: 12/05/2018
ms.keywords: CF_CALLBACK_CANCEL_FLAGS, CF_CALLBACK_CANCEL_FLAGS enumeration, CF_CALLBACK_CANCEL_FLAG_IO_ABORTED, CF_CALLBACK_CANCEL_FLAG_IO_TIMEOUT, CF_CALLBACK_CANCEL_FLAG_NONE, cfapi/CF_CALLBACK_CANCEL_FLAGS, cfapi/CF_CALLBACK_CANCEL_FLAG_IO_ABORTED, cfapi/CF_CALLBACK_CANCEL_FLAG_IO_TIMEOUT, cfapi/CF_CALLBACK_CANCEL_FLAG_NONE, cloudApi.cf_callback_cancel_flags
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
req.typenames: CF_CALLBACK_CANCEL_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_CALLBACK_CANCEL_FLAGS
 - cfapi/CF_CALLBACK_CANCEL_FLAGS
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
 - CF_CALLBACK_CANCEL_FLAGS
---

# CF_CALLBACK_CANCEL_FLAGS enumeration


## -description

Callback flags for canceling data fetching for a placeholder file or folder.

## -enum-fields

### -field CF_CALLBACK_CANCEL_FLAG_NONE:0x00000000

No cancel flag.

### -field CF_CALLBACK_CANCEL_FLAG_IO_TIMEOUT:0x00000001

Flag to be set if the user request is cancelled as a result of the expiration of the 60 second timer.

### -field CF_CALLBACK_CANCEL_FLAG_IO_ABORTED:0x00000002

Flag to be set if the user request is cancelled as a result of the user explicitly terminating the hydration from app-initiated download toast.

