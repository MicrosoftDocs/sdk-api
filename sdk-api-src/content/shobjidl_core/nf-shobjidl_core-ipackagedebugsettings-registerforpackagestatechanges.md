---
UID: NF:shobjidl_core.IPackageDebugSettings.RegisterForPackageStateChanges
title: IPackageDebugSettings::RegisterForPackageStateChanges
author: windows-sdk-content
description: Register for package state-change notifications.
old-location: shell\IPackageDebugSettings_RegisterForPackageStateChanges.htm
old-project: shell
ms.assetid: D0E26154-DADB-499D-A434-8211196E2F5F
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],RegisterForPackageStateChanges method, IPackageDebugSettings.RegisterForPackageStateChanges, IPackageDebugSettings::RegisterForPackageStateChanges, RegisterForPackageStateChanges, RegisterForPackageStateChanges method [Windows Shell], RegisterForPackageStateChanges method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_RegisterForPackageStateChanges, shobjidl_core/IPackageDebugSettings::RegisterForPackageStateChanges
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPackageDebugSettings.RegisterForPackageStateChanges
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
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
 

 

