---
UID: NF:shobjidl_core.IPackageDebugSettings.UnregisterForPackageStateChanges
title: IPackageDebugSettings::UnregisterForPackageStateChanges method
author: windows-driver-content
description: Unregisters for changes in the state of the processes of the specified package.
old-location: winrt\ipackagedebugsettings_unregisterforpackagestatechanges.htm
old-project: WinRT
ms.assetid: 7EC7CCCB-1AE6-458C-A92C-4D303717EA15
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IPackageDebugSettings, IPackageDebugSettings interface [Windows Runtime], UnregisterForPackageStateChanges method, IPackageDebugSettings::UnregisterForPackageStateChanges, UnregisterForPackageStateChanges method [Windows Runtime], UnregisterForPackageStateChanges method [Windows Runtime], IPackageDebugSettings interface, UnregisterForPackageStateChanges,IPackageDebugSettings.UnregisterForPackageStateChanges, shobjidl_core/IPackageDebugSettings::UnregisterForPackageStateChanges, winrt.ipackagedebugsettings_unregisterforpackagestatechanges
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
-	IPackageDebugSettings.UnregisterForPackageStateChanges
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# IPackageDebugSettings::UnregisterForPackageStateChanges method


## -description


Unregisters for changes in the state of the processes of the specified package.


## -parameters




### -param dwCookie






#### - pdwCookie [in]

Type: <b>DWORD</b>

A cookie that was returned by <a href="https://msdn.microsoft.com/B53CF95C-FD40-45E2-869B-32F089986D13">RegisterForPackageStateChanges</a> to identify the registation to unregister. 


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cae72152-c9d2-4791-b3f8-1187fb2a4d6c">IPackageDebugSettings</a>
 

 

