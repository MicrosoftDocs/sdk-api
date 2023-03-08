---
UID: NF:shobjidl_core.IPackageDebugSettings.StartSessionRedirection
title: IPackageDebugSettings::StartSessionRedirection (shobjidl_core.h)
description: Causes background tasks for the specified package to activate in the specified user session.
helpviewer_keywords: ["IPackageDebugSettings interface [Windows Shell]","StartSessionRedirection method","IPackageDebugSettings.StartSessionRedirection","IPackageDebugSettings::StartSessionRedirection","StartSessionRedirection","StartSessionRedirection method [Windows Shell]","StartSessionRedirection method [Windows Shell]","IPackageDebugSettings interface","shell.IPackageDebugSettings_StartSessionRedirection","shobjidl_core/IPackageDebugSettings::StartSessionRedirection"]
old-location: shell\IPackageDebugSettings_StartSessionRedirection.htm
tech.root: shell
ms.assetid: a9f40c32-afbe-4f1f-9693-72a757d93a05
ms.date: 12/05/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],StartSessionRedirection method, IPackageDebugSettings.StartSessionRedirection, IPackageDebugSettings::StartSessionRedirection, StartSessionRedirection, StartSessionRedirection method [Windows Shell], StartSessionRedirection method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_StartSessionRedirection, shobjidl_core/IPackageDebugSettings::StartSessionRedirection
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
 - IPackageDebugSettings::StartSessionRedirection
 - shobjidl_core/IPackageDebugSettings::StartSessionRedirection
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
 - IPackageDebugSettings.StartSessionRedirection
---

# IPackageDebugSettings::StartSessionRedirection


## -description

Causes background tasks for the specified package to activate  in the specified user session.

## -parameters

### -param packageFullName [in]

The package full name.

### -param sessionId [in]

The identifier of the session which background tasks are redirected to.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-stopsessionredirection">StopSessionRedirection</a>