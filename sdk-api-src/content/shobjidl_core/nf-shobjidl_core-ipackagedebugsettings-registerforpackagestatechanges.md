---
UID: NF:shobjidl_core.IPackageDebugSettings.RegisterForPackageStateChanges
title: IPackageDebugSettings::RegisterForPackageStateChanges method
author: windows-driver-content
description: Registers for changes in the state of the processes of the specified package.
old-location: winrt\ipackagedebugsettings_registerforpackagestatechanges.htm
old-project: WinRT
ms.assetid: B53CF95C-FD40-45E2-869B-32F089986D13
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IPackageDebugSettings, IPackageDebugSettings interface [Windows Runtime], RegisterForPackageStateChanges method, IPackageDebugSettings::RegisterForPackageStateChanges, RegisterForPackageStateChanges method [Windows Runtime], RegisterForPackageStateChanges method [Windows Runtime], IPackageDebugSettings interface, RegisterForPackageStateChanges,IPackageDebugSettings.RegisterForPackageStateChanges, shobjidl_core/IPackageDebugSettings::RegisterForPackageStateChanges, winrt.ipackagedebugsettings_registerforpackagestatechanges
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: OVERLAPPED, *LPOVERLAPPED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IPackageDebugSettings.RegisterForPackageStateChanges
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IPackageDebugSettings::RegisterForPackageStateChanges method


## -description


Registers for changes in the state of the processes of the specified package.


## -parameters




### -param packageFullName [in]

Type: <b>LPCWSTR</b>

The package full name.


### -param pPackageExecutionStateChangeNotification [in]

Type: <b>IPackageExecutionStateChangeNotification*</b>

A pointer to the <a href="https://msdn.microsoft.com/6AD9A9CD-933B-432F-A124-48092588C5DF">IPackageExecutionStateChangeNotification</a> interface that represent the change notification.


### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a variable that receives the cookie that is used to unregister by calling <a href="https://msdn.microsoft.com/7EC7CCCB-1AE6-458C-A92C-4D303717EA15">UnregisterForPackageStateChanges</a>. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cae72152-c9d2-4791-b3f8-1187fb2a4d6c">IPackageDebugSettings</a>
 

 

