---
UID: NC:clfsmgmtw32.PLOG_UNPINNED_CALLBACK
title: PLOG_UNPINNED_CALLBACK (clfsmgmtw32.h)
description: The LOG_UNPINNED_CALLBACK function is an application-defined callback function that receives notification that the log has become unpinned.
helpviewer_keywords: ["LOG_UNPINNED_CALLBACK","LOG_UNPINNED_CALLBACK callback function [Files]","PLOG_UNPINNED_CALLBACK","PLOG_UNPINNED_CALLBACK callback","clfsmgmtw32/LOG_UNPINNED_CALLBACK","fs.log_unpinned_callback"]
old-location: fs\log_unpinned_callback.htm
tech.root: fs
ms.assetid: ab3b5ffb-01a5-4678-bcfa-7e71b1f4c0f3
ms.date: 12/05/2018
ms.keywords: LOG_UNPINNED_CALLBACK, LOG_UNPINNED_CALLBACK callback function [Files], PLOG_UNPINNED_CALLBACK, PLOG_UNPINNED_CALLBACK callback, clfsmgmtw32/LOG_UNPINNED_CALLBACK, fs.log_unpinned_callback
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PLOG_UNPINNED_CALLBACK
 - clfsmgmtw32/PLOG_UNPINNED_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Clfsmgmtw32.h
api_name:
 - LOG_UNPINNED_CALLBACK
---

# PLOG_UNPINNED_CALLBACK callback function


## -description

The 
<b>LOG_UNPINNED_CALLBACK</b> function is an application-defined callback function that receives notification that the log has become unpinned. The callback is invoked in the context of an asynchronous procedure call (APC)  on the thread that registers for log management.

## -parameters

### -param hLogFile [in]

The handle to the log.

### -param pvClientContext [in]

A pointer to the client context. This is the same context specified when registering the client, which is a member of <a href="/windows/desktop/api/clfsmgmtw32/ns-clfsmgmtw32-log_management_callbacks">LOG_MANAGEMENT_CALLBACKS</a>.

## -see-also

<a href="/windows/desktop/api/clfsmgmtw32/nc-clfsmgmtw32-plog_full_handler_callback">LOG_FULL_HANDLER_CALLBACK</a>