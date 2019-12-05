---
UID: NF:shobjidl_core.IPackageDebugSettings.StopServicing
title: IPackageDebugSettings::StopServicing (shobjidl_core.h)
description: Completes the previous servicing operation that was started by a call to the StartServicing method.
old-location: shell\IPackageDebugSettings_StopServicing.htm
tech.root: shell
ms.assetid: 129ea98a-e0c3-4472-918c-6d9aa4858c4b
ms.date: 12/05/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],StopServicing method, IPackageDebugSettings.StopServicing, IPackageDebugSettings::StopServicing, StopServicing, StopServicing method [Windows Shell], StopServicing method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_StopServicing, shobjidl_core/IPackageDebugSettings::StopServicing
ms.topic: method
f1_keywords:
- shobjidl_core/IPackageDebugSettings.StopServicing
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
- IPackageDebugSettings.StopServicing
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPackageDebugSettings::StopServicing


## -description


Completes the previous servicing operation that was started by a call to the  <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-startservicing">StartServicing</a> method.


## -parameters




### -param packageFullName [in]

The package full name.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-startservicing">StartServicing</a>
 

 

