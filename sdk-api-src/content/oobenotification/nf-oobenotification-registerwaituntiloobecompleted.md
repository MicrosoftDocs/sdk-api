---
UID: NF:oobenotification.RegisterWaitUntilOOBECompleted
title: RegisterWaitUntilOOBECompleted function (oobenotification.h)
description: Registers a callback to be called once OOBE (Windows Welcome) has been completed.
helpviewer_keywords: ["RegisterWaitUntilOOBECompleted","RegisterWaitUntilOOBECompleted function","oobenotification/RegisterWaitUntilOOBECompleted","windowssetupandmigration.registerwaituntiloobecompleted"]
old-location: windowssetupandmigration\registerwaituntiloobecompleted.htm
tech.root: windowssetupandmigration
ms.assetid: D1581B09-06A7-483F-929D-1AF93832942D
ms.date: 12/05/2018
ms.keywords: RegisterWaitUntilOOBECompleted, RegisterWaitUntilOOBECompleted function, oobenotification/RegisterWaitUntilOOBECompleted, windowssetupandmigration.registerwaituntiloobecompleted
req.header: oobenotification.h
req.include-header: 
req.target-type: Windows
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterWaitUntilOOBECompleted
 - oobenotification/RegisterWaitUntilOOBECompleted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-oobe-notification-l1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - RegisterWaitUntilOOBECompleted
---

# RegisterWaitUntilOOBECompleted function


## -description

Registers a callback to be called once OOBE (Windows Welcome) has been completed.

## -parameters

### -param OOBECompletedCallback

Pointer to an application-defined callback function that will be called upon completion of OOBE. For more information, see <a href="/previous-versions/windows/desktop/api/oobenotification/nc-oobenotification-oobe_completed_callback">OOBE_COMPLETED_CALLBACK</a>.

### -param CallbackContext

Pointer to the callback context. This value will be passed to the function specified by <i>OOBECompletedCallback</i>. This value can be <b>null</b>.

### -param WaitHandle

Pointer to a variable that will receive the handle to the wait callback registration.

## -returns

<b>TRUE</b> if the routine successfully registered the callback. Otherwise, <b>FALSE</b> is returned. If <b>FALSE</b>, <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will retrieve extended error information.

## -remarks

If <b>RegisterWaitUntilOOBECompleted</b> returns <b>FALSE</b>, and a subsequent call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns a value of <b>ERROR_INVALID_STATE</b>, this indicates that OOBE is already complete and there is no need to register for OOBE completion.