---
UID: NF:shobjidl_core.IPackageDebugSettings.DisableDebugging
title: IPackageDebugSettings::DisableDebugging
author: windows-sdk-content
description: Disables debug mode for the processes of the specified package.
old-location: winrt\ipackagedebugsettings_disabledebugging.htm
tech.root: WinRT
ms.assetid: ad7efefb-aacd-48fa-bfe6-26271bd03b86
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DisableDebugging, DisableDebugging method [Windows Runtime], DisableDebugging method [Windows Runtime],IPackageDebugSettings interface, IPackageDebugSettings interface [Windows Runtime],DisableDebugging method, IPackageDebugSettings.DisableDebugging, IPackageDebugSettings::DisableDebugging, shobjidl_core/IPackageDebugSettings::DisableDebugging, winrt.ipackagedebugsettings_disabledebugging
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
 - IPackageDebugSettings.DisableDebugging
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPackageDebugSettings::DisableDebugging


## -description


Disables debug mode for the processes of the specified package.


## -parameters




### -param packageFullName [in]

Type: <b>LPCWSTR</b>

The package full name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method has no effect if the <a href="https://msdn.microsoft.com/6219e8d7-0631-482f-b602-b0453d4b1e70">EnableDebugging</a> method was not previously called for this package.




## -see-also




<a href="https://msdn.microsoft.com/cae72152-c9d2-4791-b3f8-1187fb2a4d6c">IPackageDebugSettings</a>
 

 

