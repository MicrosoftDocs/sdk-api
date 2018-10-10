---
UID: NF:shobjidl_core.IPackageDebugSettings.StartSessionRedirection
title: IPackageDebugSettings::StartSessionRedirection
author: windows-sdk-content
description: Starts redirection for the specified session identifier.
old-location: winrt\ipackagedebugsettings_startsessionredirection.htm
tech.root: WinRT
ms.assetid: 686CF2EC-CEE7-4E6A-9E97-9DD80AE89131
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPackageDebugSettings interface [Windows Runtime],StartSessionRedirection method, IPackageDebugSettings.StartSessionRedirection, IPackageDebugSettings::StartSessionRedirection, StartSessionRedirection, StartSessionRedirection method [Windows Runtime], StartSessionRedirection method [Windows Runtime],IPackageDebugSettings interface, shobjidl_core/IPackageDebugSettings::StartSessionRedirection, winrt.ipackagedebugsettings_startsessionredirection
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IPackageDebugSettings.StartSessionRedirection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPackageDebugSettings::StartSessionRedirection


## -description


Starts redirection for the specified session identifier.


## -parameters




### -param packageFullName [in]

Type: <b>LPCWSTR</b>

The package full name.


### -param sessionId [in]

Type: <b>ULONG</b>

The session identifier.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cae72152-c9d2-4791-b3f8-1187fb2a4d6c">IPackageDebugSettings</a>
 

 

