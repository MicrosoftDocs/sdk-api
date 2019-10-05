---
UID: NF:shobjidl_core.IPackageDebugSettings.RegisterForPackageStateChanges
title: IPackageDebugSettings::RegisterForPackageStateChanges (shobjidl_core.h)
author: windows-sdk-content
description: Register for package state-change notifications.
old-location: shell\IPackageDebugSettings_RegisterForPackageStateChanges.htm
tech.root: shell
ms.assetid: D0E26154-DADB-499D-A434-8211196E2F5F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],RegisterForPackageStateChanges method, IPackageDebugSettings.RegisterForPackageStateChanges, IPackageDebugSettings::RegisterForPackageStateChanges, RegisterForPackageStateChanges, RegisterForPackageStateChanges method [Windows Shell], RegisterForPackageStateChanges method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_RegisterForPackageStateChanges, shobjidl_core/IPackageDebugSettings::RegisterForPackageStateChanges
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IPackageDebugSettings.RegisterForPackageStateChanges"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPackageDebugSettings.RegisterForPackageStateChanges
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPackageDebugSettings::RegisterForPackageStateChanges


## -description


Register for package state-change notifications.


## -parameters




### -param packageFullName [in]

The package full name.


### -param pPackageExecutionStateChangeNotification [in]

Package state-change notifications are delivered by the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackageexecutionstatechangenotification-onstatechanged">OnStateChanged</a> function on <i>pPackageExecutionStateChangeNotification</i>.


### -param pdwCookie [out]

A unique registration identifier for the current listener. Use this identifier  to unregister for package state-change notifications by using the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-unregisterforpackagestatechanges">UnregisterForPackageStateChanges</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Notifications are raised when the package enters the running,
suspending, and
suspended states.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackageexecutionstatechangenotification">IPackageExecutionStateChangeNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-unregisterforpackagestatechanges">UnregisterForPackageStateChanges</a>
 

 

