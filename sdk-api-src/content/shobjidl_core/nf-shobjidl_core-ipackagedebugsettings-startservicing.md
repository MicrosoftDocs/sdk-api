---
UID: NF:shobjidl_core.IPackageDebugSettings.StartServicing
title: IPackageDebugSettings::StartServicing (shobjidl_core.h)
description: Suspends and terminates the non-background portion of the apps associated with the specified package and cancels the background tasks associated with the package.
helpviewer_keywords: ["IPackageDebugSettings interface [Windows Shell]","StartServicing method","IPackageDebugSettings.StartServicing","IPackageDebugSettings::StartServicing","StartServicing","StartServicing method [Windows Shell]","StartServicing method [Windows Shell]","IPackageDebugSettings interface","shell.IPackageDebugSettings_StartServicing","shobjidl_core/IPackageDebugSettings::StartServicing"]
old-location: shell\IPackageDebugSettings_StartServicing.htm
tech.root: shell
ms.assetid: 40f5331d-194f-4beb-9c59-f6899186b393
ms.date: 12/05/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],StartServicing method, IPackageDebugSettings.StartServicing, IPackageDebugSettings::StartServicing, StartServicing, StartServicing method [Windows Shell], StartServicing method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_StartServicing, shobjidl_core/IPackageDebugSettings::StartServicing
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
 - IPackageDebugSettings::StartServicing
 - shobjidl_core/IPackageDebugSettings::StartServicing
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
 - IPackageDebugSettings.StartServicing
---

# IPackageDebugSettings::StartServicing


## -description

Suspends and terminates the non-background portion of the apps associated with the specified package and cancels the background tasks associated with the package.

## -parameters

### -param packageFullName [in]

The package full name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use the <b>StartServicing</b> method to simulate what happens when a package is updated to a newer version. New background task activations are buffered (delayed) until you call the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-stopservicing">StopServicing</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-stopservicing">StopServicing</a>