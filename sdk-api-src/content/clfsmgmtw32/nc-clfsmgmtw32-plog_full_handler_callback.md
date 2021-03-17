---
UID: NC:clfsmgmtw32.PLOG_FULL_HANDLER_CALLBACK
title: PLOG_FULL_HANDLER_CALLBACK (clfsmgmtw32.h)
description: The LOG_FULL_HANDLER_CALLBACK function is an application-defined callback function that receives notification that the call to HandleLogFull is complete.
helpviewer_keywords: ["LOG_FULL_HANDLER_CALLBACK","LOG_FULL_HANDLER_CALLBACK callback function [Files]","PLOG_FULL_HANDLER_CALLBACK","PLOG_FULL_HANDLER_CALLBACK callback","clfsmgmtw32/ LOG_FULL_HANDLER_CALLBACK","fs.log_full_handler_callback"]
old-location: fs\log_full_handler_callback.htm
tech.root: fs
ms.assetid: 7b8d3b94-2b2e-427e-9b89-530310ecc6fe
ms.date: 12/05/2018
ms.keywords: LOG_FULL_HANDLER_CALLBACK, LOG_FULL_HANDLER_CALLBACK callback function [Files], PLOG_FULL_HANDLER_CALLBACK, PLOG_FULL_HANDLER_CALLBACK callback, clfsmgmtw32/ LOG_FULL_HANDLER_CALLBACK, fs.log_full_handler_callback
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
 - PLOG_FULL_HANDLER_CALLBACK
 - clfsmgmtw32/PLOG_FULL_HANDLER_CALLBACK
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
 - LOG_FULL_HANDLER_CALLBACK
---

# PLOG_FULL_HANDLER_CALLBACK callback function


## -description

The 
<b>LOG_FULL_HANDLER_CALLBACK</b> function is an application-defined callback function that receives notification that the call to <a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-handlelogfull">HandleLogFull</a> is complete. The callback is invoked in the context of an asynchronous procedure call (APC) on the thread that registered for log management.

## -parameters

### -param hLogFile [in]

The handle to the log.

### -param dwError [in]

The status of the operation.

### -param fLogIsPinned [in]

Specifies if the log is considered "pinned". If <i>fLogIsPinned</i> is <b>TRUE</b> and the log is then unpinned, the <a href="/windows/desktop/api/clfsmgmtw32/nc-clfsmgmtw32-plog_unpinned_callback">LOG_UNPINNED_CALLBACK</a> is invoked.

### -param pvClientContext [in]

A pointer to the client context.

## -remarks

The client application determines which actions this callback function performs.

## -see-also

<a href="/windows/desktop/api/clfsmgmtw32/nc-clfsmgmtw32-plog_unpinned_callback">LOG_UNPINNED_CALLBACK</a>