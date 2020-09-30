---
UID: NC:clfsmgmtw32.PLOG_TAIL_ADVANCE_CALLBACK
title: PLOG_TAIL_ADVANCE_CALLBACK (clfsmgmtw32.h)
description: The LOG_TAIL_ADVANCE_CALLBACK function is an application-defined callback function that advances the log tail. The callback is invoked in the context of an asynchronous procedure call (APC) on the thread that registers for log management.
helpviewer_keywords: ["LOG_TAIL_ADVANCE_CALLBACK","LOG_TAIL_ADVANCE_CALLBACK callback function [Files]","PLOG_TAIL_ADVANCE_CALLBACK","PLOG_TAIL_ADVANCE_CALLBACK callback","clfsmgmtw32/LOG_TAIL_ADVANCE_CALLBACK","fs.log_tail_advance_callback"]
old-location: fs\log_tail_advance_callback.htm
tech.root: fs
ms.assetid: dfa64e5e-55ef-4102-90d5-104b1a624267
ms.date: 12/05/2018
ms.keywords: LOG_TAIL_ADVANCE_CALLBACK, LOG_TAIL_ADVANCE_CALLBACK callback function [Files], PLOG_TAIL_ADVANCE_CALLBACK, PLOG_TAIL_ADVANCE_CALLBACK callback, clfsmgmtw32/LOG_TAIL_ADVANCE_CALLBACK, fs.log_tail_advance_callback
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
 - PLOG_TAIL_ADVANCE_CALLBACK
 - clfsmgmtw32/PLOG_TAIL_ADVANCE_CALLBACK
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
 - LOG_TAIL_ADVANCE_CALLBACK
---

# PLOG_TAIL_ADVANCE_CALLBACK callback function


## -description

The 
<b>LOG_TAIL_ADVANCE_CALLBACK</b> function is an application-defined callback function that advances the log tail. The callback is invoked in the context of an asynchronous procedure call (APC) on the thread that registers for log management.

## -parameters

### -param hLogFile [in]

The handle to the log.

### -param lsnTarget [in]

Specifies the log sequence number (LSN) to which the client is advised to advance to or beyond. The <i>lsnTarget</i> may not refer to an actual record in the log.

### -param pvClientContext [in]

A pointer to the client context.

## -remarks

This callback can be invoked at any time. This callback function should advance the base LSN of the log to greater than or equal to the value of <i>lsnTarget</i>.

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-advancelogbase">AdvanceLogBase</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-writelogrestartarea">WriteLogRestartArea</a>