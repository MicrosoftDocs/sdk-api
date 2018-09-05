---
UID: NF:oobenotification.UnregisterWaitUntilOOBECompleted
title: UnregisterWaitUntilOOBECompleted function
author: windows-sdk-content
description: Unregisters the callback previously registered via RegisterWaitUntilOOBECompleted.
old-location: windowssetupandmigration\unregisterwaituntiloobecompleted.htm
old-project: WNF
ms.assetid: 966803DF-744A-430F-86C0-F6ACA754C603
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: UnregisterWaitUntilOOBECompleted, UnregisterWaitUntilOOBECompleted function, oobenotification/UnregisterWaitUntilOOBECompleted, windowssetupandmigration.unregisterwaituntiloobecompleted
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oobenotification.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: NET_INTERFACE_CONTEXT_TABLE
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# UnregisterWaitUntilOOBECompleted function


## -description


Unregisters the callback previously registered via <a href="https://msdn.microsoft.com/D1581B09-06A7-483F-929D-1AF93832942D">RegisterWaitUntilOOBECompleted</a>.


## -parameters




### -param WaitHandle

Handle to be unregistered.


## -returns



<b>TRUE</b> if the callback was successfully unregistered. Otherwise, <b>FALSE</b> is returned. If <b>FALSE</b>, <a href=" http://go.microsoft.com/fwlink/p/?LinkID=329935">GetLastError</a> will retrieve extended error information.



