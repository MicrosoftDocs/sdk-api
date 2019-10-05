---
UID: NE:combaseapi.CWMO_FLAGS
title: CWMO_FLAGS (combaseapi.h)
author: windows-sdk-content
description: Provides flags for the CoWaitForMultipleObjects function.
old-location: com\cwmo_flags.htm
tech.root: com
ms.assetid: 5FE605A9-DE92-4CD9-9390-6C9F5189A7CB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CWMO_DEFAULT, CWMO_DISPATCH_CALLS, CWMO_DISPATCH_WINDOW_MESSAGE, CWMO_FLAGS, CWMO_FLAGS enumeration [COM], com.cwmo_flags, combaseapi/CWMO_DEFAULT, combaseapi/CWMO_DISPATCH_CALLS, combaseapi/CWMO_DISPATCH_WINDOW_MESSAGE, combaseapi/CWMO_FLAGS
ms.topic: enum
f1_keywords: 
 - "combaseapi/CWMO_FLAGS"
dev_langs:
 - c++
req.header: combaseapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - combaseapi.h
api_name:
 - CWMO_FLAGS
targetos: Windows
req.typenames: CWMO_FLAGS
req.redist: 
ms.custom: 19H1
---

# CWMO_FLAGS enumeration


## -description


Provides flags for the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultipleobjects">CoWaitForMultipleObjects</a> function.


## -enum-fields




### -field CWMO_DEFAULT

No call dispatch.


### -field CWMO_DISPATCH_CALLS

Dispatch calls from <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultipleobjects">CoWaitForMultipleObjects</a> (default is no call dispatch).


### -field CWMO_DISPATCH_WINDOW_MESSAGES




#### - CWMO_DISPATCH_WINDOW_MESSAGE

Enable dispatch of window messages from <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cowaitformultipleobjects">CoWaitForMultipleObjects</a> in a ASTA or STA (default in ASTA is no window messages dispatched, default in STA is only a small set of special-cased messages dispatched). The value has no meaning in MTA and is ignored.

