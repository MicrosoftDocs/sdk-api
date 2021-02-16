---
UID: NS:clfsmgmtw32._LOG_MANAGEMENT_CALLBACKS
title: LOG_MANAGEMENT_CALLBACKS (clfsmgmtw32.h)
description: The LOG_MANAGEMENT_CALLBACKS structure is used to register with the Common Log File System (CLFS) for the callbacks that a client program requires information from.
helpviewer_keywords: ["*PLOG_MANAGEMENT_CALLBACKS","LOG_MANAGEMENT_CALLBACKS","LOG_MANAGEMENT_CALLBACKS structure [Files]","PLOG_MANAGEMENT_CALLBACKS","PLOG_MANAGEMENT_CALLBACKS structure pointer [Files]","clfsmgmtw32/LOG_MANAGEMENT_CALLBACKS","clfsmgmtw32/PLOG_MANAGEMENT_CALLBACKS","fs.log_management_callbacks"]
old-location: fs\log_management_callbacks.htm
tech.root: fs
ms.assetid: 69c657e7-97f0-468a-b349-9891a771c1ed
ms.date: 12/05/2018
ms.keywords: '*PLOG_MANAGEMENT_CALLBACKS, LOG_MANAGEMENT_CALLBACKS, LOG_MANAGEMENT_CALLBACKS structure [Files], PLOG_MANAGEMENT_CALLBACKS, PLOG_MANAGEMENT_CALLBACKS structure pointer [Files], clfsmgmtw32/LOG_MANAGEMENT_CALLBACKS, clfsmgmtw32/PLOG_MANAGEMENT_CALLBACKS, fs.log_management_callbacks'
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
targetos: Windows
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _LOG_MANAGEMENT_CALLBACKS
 - clfsmgmtw32/_LOG_MANAGEMENT_CALLBACKS
 - PLOG_MANAGEMENT_CALLBACKS
 - clfsmgmtw32/PLOG_MANAGEMENT_CALLBACKS
 - LOG_MANAGEMENT_CALLBACKS
 - clfsmgmtw32/LOG_MANAGEMENT_CALLBACKS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Clfsmgmtw32.h
api_name:
 - LOG_MANAGEMENT_CALLBACKS
---

# LOG_MANAGEMENT_CALLBACKS structure


## -description

The <b>LOG_MANAGEMENT_CALLBACKS</b> structure is used to register with the Common Log File System (CLFS) for the callbacks that a client program requires information from.

## -struct-fields

### -field CallbackContext

A pointer to the context which is a client-defined value.  CLFS ignores this value other than to pass it with every callback to the client.

### -field AdvanceTailCallback

 Called when the management functionality determines that the client should advance the tail of its log.

### -field LogFullHandlerCallback

Called when an asynchronous request is initiated when <a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-handlelogfull">HandleLogFull</a> completes.

### -field LogUnpinnedCallback

Called when a pinned log becomes unpinned.