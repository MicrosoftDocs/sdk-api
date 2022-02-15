---
UID: NC:winnt.PAPCFUNC
title: PAPCFUNC (winnt.h)
description: An application-defined completion routine. Specify this address when calling the QueueUserAPC function.
helpviewer_keywords: ["APCProc","APCProc callback","APCProc callback function","PAPCFUNC","_win32_apcproc","base.apcproc","winnt/APCProc"]
old-location: base\apcproc.htm
tech.root: backup
ms.assetid: 8d52ad73-0172-4d1d-b625-39629e7f5823
ms.date: 12/05/2018
ms.keywords: APCProc, APCProc callback, APCProc callback function, PAPCFUNC, _win32_apcproc, base.apcproc, winnt/APCProc
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - PAPCFUNC
 - winnt/PAPCFUNC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winnt.h
api_name:
 - APCProc
---

# PAPCFUNC callback function

## -description

An application-defined completion routine. Specify this address when calling the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc">QueueUserAPC</a> function. The <b>PAPCFUNC</b> type defines a pointer to this callback function. <b>APCProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param Parameter [in]

The data passed to the function using the <i>dwData</i> parameter of the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc">QueueUserAPC</a> function.

## -see-also

<a href="/windows/desktop/Sync/asynchronous-procedure-calls">Asynchronous Procedure Calls</a>

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc">QueueUserAPC</a>

<a href="/windows/desktop/Sync/synchronization-functions">Synchronization Functions</a>