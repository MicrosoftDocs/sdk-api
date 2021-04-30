---
UID: NF:clfsmgmtw32.HandleLogFull
title: HandleLogFull function (clfsmgmtw32.h)
description: Called by a managed log client when an attempt to reserve or append to a log fails with a log full error message. The log manager attempts to resolve the log full condition for the client, and notifies the client when the outcome is known.
helpviewer_keywords: ["HandleLogFull","HandleLogFull function [Files]","clfsmgmtw32/HandleLogFull","fs.handlelogfull"]
old-location: fs\handlelogfull.htm
tech.root: fs
ms.assetid: ed4b067f-9386-4bec-a6dc-b22d6fd52390
ms.date: 12/05/2018
ms.keywords: HandleLogFull, HandleLogFull function [Files], clfsmgmtw32/HandleLogFull, fs.handlelogfull
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
 - HandleLogFull
 - clfsmgmtw32/HandleLogFull
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
 - HandleLogFull
---

# HandleLogFull function


## -description

The <b>HandleLogFull</b> function is called by a managed log client when an attempt to reserve or append to a log fails with a log full error message.  The log manager attempts to resolve the log full condition for the client, and notifies the client when the outcome is known. As a result of this call, the log may get larger in size.

## -parameters

### -param hLog [in]

A handle to the log on which to resolve the log full condition. The handle must have been registered with <a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-registermanageablelogclient">RegisterManageableLogClient</a>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Valid values include the following:

## -remarks

If containers are created to resolve a log-full condition, they are created using the calling application's security context.

<b>HandleLogFull</b> always results in asynchronous behavior or an error; if it returns false and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_IO_PENDING</b>, the result is asynchronous behavior. If a request is asynchronous, a notification is sent to the client when the handler has either  resolved the log full condition or it fails.