---
UID: NE:cfapi.CF_CALLBACK_CLOSE_COMPLETION_FLAGS
title: CF_CALLBACK_CLOSE_COMPLETION_FLAGS
author: windows-sdk-content
description: Callback flags for notifying a sync provider that a placeholder under one of its sync roots that has been previously opened for read/write/delete access is now closed.
old-location: cloudapi\cf_callback_close_completion_flags.htm
tech.root: cfApi
ms.assetid: D80D95FB-C53B-4A31-97B9-389BE73BE966
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: CF_CALLBACK_CLOSE_COMPLETION_FLAGS, CF_CALLBACK_CLOSE_COMPLETION_FLAGS enumeration, CF_CALLBACK_CLOSE_COMPLETION_FLAG_DELETED, CF_CALLBACK_CLOSE_COMPLETION_FLAG_NONE, cfapi/CF_CALLBACK_CLOSE_COMPLETION_FLAGS, cfapi/CF_CALLBACK_CLOSE_COMPLETION_FLAG_DELETED, cfapi/CF_CALLBACK_CLOSE_COMPLETION_FLAG_NONE, cloudApi.cf_callback_close_completion_flags
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
 - CF_CALLBACK_CLOSE_COMPLETION_FLAGS
product: Windows
targetos: Windows
req.typenames: CF_CALLBACK_CLOSE_COMPLETION_FLAGS
req.redist: 
---

# CF_CALLBACK_CLOSE_COMPLETION_FLAGS enumeration


## -description


Callback flags for notifying a sync provider that a placeholder under one of its sync roots that has been previously opened for read/write/delete access is now closed. 


## -enum-fields




### -field CF_CALLBACK_CLOSE_COMPLETION_FLAG_NONE

No close completion flags.


### -field CF_CALLBACK_CLOSE_COMPLETION_FLAG_DELETED

A flag set if a placeholder is deleted as a result of the close.

