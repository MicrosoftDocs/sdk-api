---
UID: NS:clfsmgmtw32._LOG_MANAGEMENT_CALLBACKS
title: "_LOG_MANAGEMENT_CALLBACKS"
author: windows-sdk-content
description: The LOG_MANAGEMENT_CALLBACKS structure is used to register with the Common Log File System (CLFS) for the callbacks that a client program requires information from.
old-location: fs\log_management_callbacks.htm
tech.root: Clfs
ms.assetid: 69c657e7-97f0-468a-b349-9891a771c1ed
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PLOG_MANAGEMENT_CALLBACKS, LOG_MANAGEMENT_CALLBACKS, LOG_MANAGEMENT_CALLBACKS structure [Files], PLOG_MANAGEMENT_CALLBACKS, PLOG_MANAGEMENT_CALLBACKS structure pointer [Files], _LOG_MANAGEMENT_CALLBACKS, clfsmgmtw32/LOG_MANAGEMENT_CALLBACKS, clfsmgmtw32/PLOG_MANAGEMENT_CALLBACKS, fs.log_management_callbacks"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: clfsmgmtw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
 - Clfsmgmtw32.h
api_name:
 - LOG_MANAGEMENT_CALLBACKS
product: Windows
targetos: Windows
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
req.redist: 
---

# _LOG_MANAGEMENT_CALLBACKS structure


## -description


The <b>LOG_MANAGEMENT_CALLBACKS</b> structure is used to register with the Common Log File System (CLFS) for the callbacks that a client program requires information from.


## -struct-fields




### -field CallbackContext

A pointer to the context which is a client-defined value.  CLFS ignores this value other than to pass it with every callback to the client.


### -field AdvanceTailCallback

 Called when the management functionality determines that the client should advance the tail of its log.


### -field LogFullHandlerCallback

Called when an asynchronous request is initiated when <a href="https://msdn.microsoft.com/ed4b067f-9386-4bec-a6dc-b22d6fd52390">HandleLogFull</a> completes.


### -field LogUnpinnedCallback

Called when a pinned log becomes unpinned.

