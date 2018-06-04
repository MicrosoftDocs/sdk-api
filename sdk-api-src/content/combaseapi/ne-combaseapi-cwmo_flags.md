---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# CWMO_FLAGS enumeration


## -description


Provides flags for the <a href="https://msdn.microsoft.com/7A14E4F4-20F0-43FF-8D64-9AAC34B8D56F">CoWaitForMultipleObjects</a> function.


## -enum-fields




### -field CWMO_DEFAULT


### -field CWMO_DISPATCH_CALLS

Dispatch calls from <a href="https://msdn.microsoft.com/7A14E4F4-20F0-43FF-8D64-9AAC34B8D56F">CoWaitForMultipleObjects</a> (default is no call dispatch).


### -field CWMO_DISPATCH_WINDOW_MESSAGES




#### - CWMO_DISPATCH_WINDOW_MESSAGE

Enable dispatch of window messages from <a href="https://msdn.microsoft.com/7A14E4F4-20F0-43FF-8D64-9AAC34B8D56F">CoWaitForMultipleObjects</a> in a ASTA or STA (default in ASTA is no window messages dispatched, default in STA is only a small set of special-cased messages dispatched). The value has no meaning in MTA and is ignored.

