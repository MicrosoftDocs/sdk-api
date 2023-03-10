---
UID: NF:shobjidl_core.IPackageDebugSettings.DisableDebugging
title: IPackageDebugSettings::DisableDebugging (shobjidl_core.h)
description: Disables debug mode for the processes of the specified package.
helpviewer_keywords: ["DisableDebugging","DisableDebugging method [Windows Shell]","DisableDebugging method [Windows Shell]","IPackageDebugSettings interface","IPackageDebugSettings interface [Windows Shell]","DisableDebugging method","IPackageDebugSettings.DisableDebugging","IPackageDebugSettings::DisableDebugging","shell.IPackageDebugSettings_DisableDebugging","shobjidl_core/IPackageDebugSettings::DisableDebugging"]
old-location: shell\IPackageDebugSettings_DisableDebugging.htm
tech.root: shell
ms.assetid: 102e57be-296e-44ec-8211-f2c2d5eae1e6
ms.date: 12/05/2018
ms.keywords: DisableDebugging, DisableDebugging method [Windows Shell], DisableDebugging method [Windows Shell],IPackageDebugSettings interface, IPackageDebugSettings interface [Windows Shell],DisableDebugging method, IPackageDebugSettings.DisableDebugging, IPackageDebugSettings::DisableDebugging, shell.IPackageDebugSettings_DisableDebugging, shobjidl_core/IPackageDebugSettings::DisableDebugging
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
 - IPackageDebugSettings::DisableDebugging
 - shobjidl_core/IPackageDebugSettings::DisableDebugging
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
 - IPackageDebugSettings.DisableDebugging
---

# IPackageDebugSettings::DisableDebugging


## -description

Disables debug mode for the processes of the specified package.

## -parameters

### -param packageFullName [in]

The package full name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method has no effect if the <a href="/previous-versions/hh438395(v=vs.85)">EnableDebugging</a> method was not previously called for this package.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-enabledebugging">EnableDebugging</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>