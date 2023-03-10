---
UID: NF:clfsmgmtw32.ReadLogNotification
title: ReadLogNotification function (clfsmgmtw32.h)
description: Retrieves notifications from the log manager. It retrieves a queued notification from the log manager immediately if a notification is available; otherwise the request remains pending until a notification is generated.
helpviewer_keywords: ["ReadLogNotification","ReadLogNotification function [Files]","clfsmgmtw32/ReadLogNotification","fs.readlognotification"]
old-location: fs\readlognotification.htm
tech.root: fs
ms.assetid: 08931011-511b-471b-9a4a-ebc96e963c51
ms.date: 12/05/2018
ms.keywords: ReadLogNotification, ReadLogNotification function [Files], clfsmgmtw32/ReadLogNotification, fs.readlognotification
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
 - ReadLogNotification
 - clfsmgmtw32/ReadLogNotification
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
 - ReadLogNotification
---

# ReadLogNotification function


## -description

The <b>ReadLogNotification</b> function retrieves notifications from the log manager. It retrieves a queued notification from the log manager immediately if a notification is available; otherwise the request remains pending until a notification is generated.

## -parameters

### -param hLog [in]

The handle to the log.

### -param pNotification [out]

Receives the notification type, and if the type has parameters associated with it, the parameters.

### -param lpOverlapped [in]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that is required for asynchronous operation. If asynchronous operation is not used, this parameter can be <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following is a possible error code:

## -remarks

If the log handle is not created with the <b>FILE_FLAG_OVERLAPPED</b> file option, no operations can start on the log handle while the call to <b>ReadLogNotification</b>  is pending.

## -see-also

<a href="/windows/desktop/api/clfsmgmt/ns-clfsmgmt-clfs_mgmt_notification">CLFS_MGMT_NOTIFICATION</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>