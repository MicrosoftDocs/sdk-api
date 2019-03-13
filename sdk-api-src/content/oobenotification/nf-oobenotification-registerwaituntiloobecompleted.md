---
UID: NF:oobenotification.RegisterWaitUntilOOBECompleted
title: RegisterWaitUntilOOBECompleted function
author: windows-sdk-content
description: Registers a callback to be called once OOBE (Windows Welcome) has been completed.
old-location: windowssetupandmigration\registerwaituntiloobecompleted.htm
tech.root: WNF
ms.assetid: D1581B09-06A7-483F-929D-1AF93832942D
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RegisterWaitUntilOOBECompleted, RegisterWaitUntilOOBECompleted function, oobenotification/RegisterWaitUntilOOBECompleted, windowssetupandmigration.registerwaituntiloobecompleted
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RegisterWaitUntilOOBECompleted function


## -description


Registers a callback to be called once OOBE (Windows Welcome) has been completed.


## -parameters




### -param OOBECompletedCallback

Pointer to an application-defined callback function that will be called upon completion of OOBE. For more information, see <a href="https://msdn.microsoft.com/9786D6C3-82B1-4546-9BE9-7705AD3B7DBD">OOBE_COMPLETED_CALLBACK</a>.


### -param CallbackContext

Pointer to the callback context. This value will be passed to the function specified by <i>OOBECompletedCallback</i>. This value can be <b>nulll</b>.


### -param WaitHandle

Pointer to a variable that will receive the handle to the wait callback registration.


## -returns



<b>TRUE</b> if the routine successfully registered the callback. Otherwise, <b>FALSE</b> is returned. If <b>FALSE</b>, <a href="http://go.microsoft.com/fwlink/p/?LinkID=329935">GetLastError</a> will retrieve extended error information.




## -remarks



If <b>RegisterWaitUntilOOBECompleted</b> returns <b>FALSE</b>, and a subsequent call to <a href="http://go.microsoft.com/fwlink/p/?LinkID=329935">GetLastError</a> returns a value of <b>ERROR_INVALID_STATE</b>, this indicates that OOBE is already complete and there is no need to register for OOBE completion.



