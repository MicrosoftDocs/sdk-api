---
UID: NF:shobjidl_core.IPackageDebugSettings.DisableDebugging
title: IPackageDebugSettings::DisableDebugging
author: windows-sdk-content
description: Disables debug mode for the processes of the specified package.
old-location: shell\IPackageDebugSettings_DisableDebugging.htm
tech.root: shell
ms.assetid: 102e57be-296e-44ec-8211-f2c2d5eae1e6
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: DisableDebugging, DisableDebugging method [Windows Shell], DisableDebugging method [Windows Shell],IPackageDebugSettings interface, IPackageDebugSettings interface [Windows Shell],DisableDebugging method, IPackageDebugSettings.DisableDebugging, IPackageDebugSettings::DisableDebugging, shell.IPackageDebugSettings_DisableDebugging, shobjidl_core/IPackageDebugSettings::DisableDebugging
ms.prod: windows-hardware
ms.technology: windows-devices
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

The package full name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method has no effect if the <a href="https://msdn.microsoft.com/6219e8d7-0631-482f-b602-b0453d4b1e70">EnableDebugging</a> method was not previously called for this package.




## -see-also




<a href="https://msdn.microsoft.com/a3afae41-b46e-47c8-95bb-a0aa747c6353">EnableDebugging</a>



<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>
 

 

