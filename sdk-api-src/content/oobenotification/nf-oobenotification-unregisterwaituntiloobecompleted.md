---
UID: NF:oobenotification.UnregisterWaitUntilOOBECompleted
title: UnregisterWaitUntilOOBECompleted function (oobenotification.h)
description: Unregisters the callback previously registered via RegisterWaitUntilOOBECompleted.helpviewer_keywords: ["UnregisterWaitUntilOOBECompleted","UnregisterWaitUntilOOBECompleted function","oobenotification/UnregisterWaitUntilOOBECompleted","windowssetupandmigration.unregisterwaituntiloobecompleted"]
old-location: windowssetupandmigration\unregisterwaituntiloobecompleted.htm
tech.root: WNF
ms.assetid: 966803DF-744A-430F-86C0-F6ACA754C603
ms.date: 12/05/2018
ms.keywords: UnregisterWaitUntilOOBECompleted, UnregisterWaitUntilOOBECompleted function, oobenotification/UnregisterWaitUntilOOBECompleted, windowssetupandmigration.unregisterwaituntiloobecompleted
f1_keywords:
- oobenotification/UnregisterWaitUntilOOBECompleted
dev_langs:
- c++
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
- UnregisterWaitUntilOOBECompleted
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UnregisterWaitUntilOOBECompleted function


## -description


Unregisters the callback previously registered via <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oobenotification/nf-oobenotification-registerwaituntiloobecompleted">RegisterWaitUntilOOBECompleted</a>.


## -parameters




### -param WaitHandle

Handle to be unregistered.


## -returns



<b>TRUE</b> if the callback was successfully unregistered. Otherwise, <b>FALSE</b> is returned. If <b>FALSE</b>, <a href="https://msdn.microsoft.com/library/windows/desktop/ms679360(v=vs.85).aspx">GetLastError</a> will retrieve extended error information.



