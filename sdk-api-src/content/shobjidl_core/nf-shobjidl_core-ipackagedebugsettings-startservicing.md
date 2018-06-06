---
UID: NF:shobjidl_core.IPackageDebugSettings.StartServicing
title: IPackageDebugSettings::StartServicing
author: windows-sdk-content
description: Suspends and terminates the non-background portion of the apps associated with the specified package and cancels the background tasks associated with the package.
old-location: shell\IPackageDebugSettings_StartServicing.htm
old-project: shell
ms.assetid: 40f5331d-194f-4beb-9c59-f6899186b393
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],StartServicing method, IPackageDebugSettings.StartServicing, IPackageDebugSettings::StartServicing, StartServicing, StartServicing method [Windows Shell], StartServicing method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_StartServicing, shobjidl_core/IPackageDebugSettings::StartServicing
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
 - IPackageDebugSettings.StartServicing
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IPackageDebugSettings::StartServicing


## -description


Suspends and terminates the non-background portion of the apps associated with the specified package and cancels the background tasks associated with the package.


## -parameters




### -param packageFullName [in]

The package full name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use the <b>StartServicing</b> method to simulate what happens when a package is updated to a newer version. New background task activations are buffered (delayed) until you call the <a href="https://msdn.microsoft.com/129ea98a-e0c3-4472-918c-6d9aa4858c4b">StopServicing</a> method.




## -see-also




<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>



<a href="https://msdn.microsoft.com/129ea98a-e0c3-4472-918c-6d9aa4858c4b">StopServicing</a>
 

 

