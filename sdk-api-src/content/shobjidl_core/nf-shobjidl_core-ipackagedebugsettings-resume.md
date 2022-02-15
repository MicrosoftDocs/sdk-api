---
UID: NF:shobjidl_core.IPackageDebugSettings.Resume
title: IPackageDebugSettings::Resume (shobjidl_core.h)
description: Resumes the processes of the package if they are currently suspended.
helpviewer_keywords: ["IPackageDebugSettings interface [Windows Shell]","Resume method","IPackageDebugSettings.Resume","IPackageDebugSettings::Resume","Resume","Resume method [Windows Shell]","Resume method [Windows Shell]","IPackageDebugSettings interface","shell.IPackageDebugSettings_Resume","shobjidl_core/IPackageDebugSettings::Resume"]
old-location: shell\IPackageDebugSettings_Resume.htm
tech.root: shell
ms.assetid: 2f0b3188-4c58-4ff6-983e-912131a7c934
ms.date: 12/05/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],Resume method, IPackageDebugSettings.Resume, IPackageDebugSettings::Resume, Resume, Resume method [Windows Shell], Resume method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_Resume, shobjidl_core/IPackageDebugSettings::Resume
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPackageDebugSettings::Resume
 - shobjidl_core/IPackageDebugSettings::Resume
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl_core.h
api_name:
 - IPackageDebugSettings.Resume
---

# IPackageDebugSettings::Resume


## -description

Resumes the processes of the package if they are currently suspended.

## -parameters

### -param packageFullName [in]

The package full name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Each process receives the <a href="/uwp/api/windows.applicationmodel.core.coreapplication.resuming">Resuming</a> event, which is useful for stepping through your apps as they respond to this event.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-suspend">Suspend</a>