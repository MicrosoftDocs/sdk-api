---
UID: NF:shobjidl_core.IPackageDebugSettings.Resume
title: IPackageDebugSettings::Resume
author: windows-sdk-content
description: Resumes the processes of the package if they are currently suspended.
old-location: shell\IPackageDebugSettings_Resume.htm
tech.root: shell
ms.assetid: 2f0b3188-4c58-4ff6-983e-912131a7c934
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],Resume method, IPackageDebugSettings.Resume, IPackageDebugSettings::Resume, Resume, Resume method [Windows Shell], Resume method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_Resume, shobjidl_core/IPackageDebugSettings::Resume
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
 - IPackageDebugSettings.Resume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPackageDebugSettings::Resume


## -description


Resumes the processes of the package if they are currently suspended.


## -parameters




### -param packageFullName [in]

The package full name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Each process receives the <a href="https://msdn.microsoft.com/f641f451-964b-4a84-9f8d-b33a26608df9">Resuming</a> event, which is useful for stepping through your apps as they respond to this event.




## -see-also




<a href="https://msdn.microsoft.com/e407c4ca-0de1-4b17-bb83-5c4128952d48">IPackageDebugSettings</a>



<a href="https://msdn.microsoft.com/b1a62712-cd03-4728-b0f1-c1b543f2e056">Suspend</a>
 

 

