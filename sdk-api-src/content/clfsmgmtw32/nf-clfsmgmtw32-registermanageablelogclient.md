---
UID: NF:clfsmgmtw32.RegisterManageableLogClient
title: RegisterManageableLogClient function (clfsmgmtw32.h)
description: Registers a client with the log manager. A client can specify whether to receive notifications by using callbacks, or have the notifications queued for retrieval by using ReadLogNotification.
helpviewer_keywords: ["RegisterManageableLogClient","RegisterManageableLogClient function [Files]","clfsmgmtw32/RegisterManageableLogClient","fs.registermanageablelogclient"]
old-location: fs\registermanageablelogclient.htm
tech.root: fs
ms.assetid: ca7969a1-e391-4e3f-96a8-5fb23c400d7e
ms.date: 12/05/2018
ms.keywords: RegisterManageableLogClient, RegisterManageableLogClient function [Files], clfsmgmtw32/RegisterManageableLogClient, fs.registermanageablelogclient
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
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterManageableLogClient
 - clfsmgmtw32/RegisterManageableLogClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - RegisterManageableLogClient
---

# RegisterManageableLogClient function


## -description

The <b>RegisterManageableLogClient</b> function registers a client with the log manager. A client can specify whether to receive notifications by using callbacks, or have the notifications  queued for retrieval by using <a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-readlognotification">ReadLogNotification</a>.

## -parameters

### -param hLog [in]

The handle to the log to register. Only one registration per unique opening of the log is allowed.

### -param pCallbacks [in]

Specifies the callbacks that the client is registering for.  Valid callbacks are enumerated by <a href="/windows/desktop/api/clfsmgmtw32/ns-clfsmgmtw32-log_management_callbacks">LOG_MANAGEMENT_CALLBACKS</a>. Specify zero to queue notifications instead.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A client can deregister either by closing the log handle, or by calling <a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-deregistermanageablelogclient">DeregisterManageableLogClient</a>.


#### Examples

For an example that uses this function, see <a href="/previous-versions/windows/desktop/clfs/creating-a-log-file">Creating a Log File</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-deregistermanageablelogclient">DeregisterManageableLogClient</a>



<a href="/windows/desktop/api/clfsmgmtw32/ns-clfsmgmtw32-log_management_callbacks">LOG_MANAGEMENT_CALLBACKS</a>