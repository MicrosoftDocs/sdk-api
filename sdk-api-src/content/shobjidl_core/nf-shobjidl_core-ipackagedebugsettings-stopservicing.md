---
UID: NF:shobjidl_core.IPackageDebugSettings.StopServicing
title: IPackageDebugSettings::StopServicing
author: windows-sdk-content
description: Completes the previous servicing operation that was started by a call to the StartServicing method.
old-location: shell\IPackageDebugSettings_StopServicing.htm
tech.root: shell
ms.assetid: 129ea98a-e0c3-4472-918c-6d9aa4858c4b
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],StopServicing method, IPackageDebugSettings.StopServicing, IPackageDebugSettings::StopServicing, StopServicing, StopServicing method [Windows Shell], StopServicing method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_StopServicing, shobjidl_core/IPackageDebugSettings::StopServicing
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
 - IPackageDebugSettings.StopServicing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPackageDebugSettings::StopServicing


## -description


Completes the previous servicing operation that was started by a call to the  <a href="https://msdn.microsoft.com/40f5331d-194f-4beb-9c59-f6899186b393">StartServicing</a> method.


## -parameters




### -param packageFullName [in]

The package full name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>



<a href="https://msdn.microsoft.com/40f5331d-194f-4beb-9c59-f6899186b393">StartServicing</a>
 

 

