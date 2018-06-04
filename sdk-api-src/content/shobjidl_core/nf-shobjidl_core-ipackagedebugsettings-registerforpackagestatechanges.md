---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IPackageDebugSettings::RegisterForPackageStateChanges


## -description


Register for package state-change notifications.


## -parameters




### -param packageFullName [in]

The package full name.


### -param pPackageExecutionStateChangeNotification [in]

Package state-change notifications are delivered by the <a href="https://msdn.microsoft.com/254986AF-4572-4D63-B055-1C05A8FB0417">OnStateChanged</a> function on <i>pPackageExecutionStateChangeNotification</i>.


### -param pdwCookie [out]

A unique registration identifier for the current listener. Use this identifier  to unregister for package state-change notifications by using the <a href="https://msdn.microsoft.com/CFCDA0AD-83D5-43DD-A7DD-C121563BF3DB">UnregisterForPackageStateChanges</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Notifications are raised when the package enters the running,
suspending, and
suspended states.




## -see-also




<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>



<a href="https://msdn.microsoft.com/6AD9A9CD-933B-432F-A124-48092588C5DF">IPackageExecutionStateChangeNotification</a>



<a href="https://msdn.microsoft.com/CFCDA0AD-83D5-43DD-A7DD-C121563BF3DB">UnregisterForPackageStateChanges</a>
 

 

