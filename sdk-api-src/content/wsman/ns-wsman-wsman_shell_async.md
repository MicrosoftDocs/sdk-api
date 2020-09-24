---
UID: NS:wsman._WSMAN_SHELL_ASYNC
title: WSMAN_SHELL_ASYNC (wsman.h)
description: Defines an asynchronous structure to be passed to all shell operations.
helpviewer_keywords: ["WSMAN_SHELL_ASYNC","WSMAN_SHELL_ASYNC structure [Windows Remote Management]","winrm.wsman_shell_async","wsman/WSMAN_SHELL_ASYNC"]
old-location: winrm\wsman_shell_async.htm
tech.root: winrm
ms.assetid: 9391e1a8-7048-49b8-9dc4-1da25b190238
ms.date: 12/05/2018
ms.keywords: WSMAN_SHELL_ASYNC, WSMAN_SHELL_ASYNC structure [Windows Remote Management], winrm.wsman_shell_async, wsman/WSMAN_SHELL_ASYNC
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: WSMAN_SHELL_ASYNC
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_SHELL_ASYNC
 - wsman/_WSMAN_SHELL_ASYNC
 - WSMAN_SHELL_ASYNC
 - wsman/WSMAN_SHELL_ASYNC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_SHELL_ASYNC
---

# WSMAN_SHELL_ASYNC structure


## -description

Defines an asynchronous structure to be passed to all shell operations. It contains an optional user context and the callback function.

## -struct-fields

### -field operationContext

Specifies the optional user context associated with the operation.

### -field completionFunction

Specifies the <a href="/windows/desktop/api/wsman/nc-wsman-wsman_shell_completion_function">WSMAN_SHELL_COMPLETION_FUNCTION</a> callback function for the operation.