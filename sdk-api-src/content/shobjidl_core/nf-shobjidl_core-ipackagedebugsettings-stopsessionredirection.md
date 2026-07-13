---
UID: NF:shobjidl_core.IPackageDebugSettings.StopSessionRedirection
title: IPackageDebugSettings::StopSessionRedirection (shobjidl_core.h)
description: Stops redirection of background tasks for the specified package.
helpviewer_keywords: ["IPackageDebugSettings interface [Windows Shell]","StopSessionRedirection method","IPackageDebugSettings.StopSessionRedirection","IPackageDebugSettings::StopSessionRedirection","StopSessionRedirection","StopSessionRedirection method [Windows Shell]","StopSessionRedirection method [Windows Shell]","IPackageDebugSettings interface","shell.IPackageDebugSettings_StopSessionRedirection","shobjidl_core/IPackageDebugSettings::StopSessionRedirection"]
old-location: shell\IPackageDebugSettings_StopSessionRedirection.htm
tech.root: shell
ms.assetid: 6edd4f9a-c9e8-45eb-a86b-a04116530aad
ms.date: 12/05/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],StopSessionRedirection method, IPackageDebugSettings.StopSessionRedirection, IPackageDebugSettings::StopSessionRedirection, StopSessionRedirection, StopSessionRedirection method [Windows Shell], StopSessionRedirection method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_StopSessionRedirection, shobjidl_core/IPackageDebugSettings::StopSessionRedirection
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
 - IPackageDebugSettings::StopSessionRedirection
 - shobjidl_core/IPackageDebugSettings::StopSessionRedirection
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
 - IPackageDebugSettings.StopSessionRedirection
---

# IPackageDebugSettings::StopSessionRedirection


## -description

Stops redirection of background tasks for the specified package.

## -parameters

### -param packageFullName [in]

The package full name.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-startsessionredirection">StartSessionRedirection</a>