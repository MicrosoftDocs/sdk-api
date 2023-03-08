---
UID: NF:shobjidl_core.IPackageDebugSettings.UnregisterForPackageStateChanges
title: IPackageDebugSettings::UnregisterForPackageStateChanges (shobjidl_core.h)
description: Stops receiving package state-change notifications associated with a previous call to RegisterForPackageStateChanges.
helpviewer_keywords: ["IPackageDebugSettings interface [Windows Shell]","UnregisterForPackageStateChanges method","IPackageDebugSettings.UnregisterForPackageStateChanges","IPackageDebugSettings::UnregisterForPackageStateChanges","UnregisterForPackageStateChanges","UnregisterForPackageStateChanges method [Windows Shell]","UnregisterForPackageStateChanges method [Windows Shell]","IPackageDebugSettings interface","shell.IPackageDebugSettings_UnregisterForPackageStateChanges","shobjidl_core/IPackageDebugSettings::UnregisterForPackageStateChanges"]
old-location: shell\IPackageDebugSettings_UnregisterForPackageStateChanges.htm
tech.root: shell
ms.assetid: CFCDA0AD-83D5-43DD-A7DD-C121563BF3DB
ms.date: 12/05/2018
ms.keywords: IPackageDebugSettings interface [Windows Shell],UnregisterForPackageStateChanges method, IPackageDebugSettings.UnregisterForPackageStateChanges, IPackageDebugSettings::UnregisterForPackageStateChanges, UnregisterForPackageStateChanges, UnregisterForPackageStateChanges method [Windows Shell], UnregisterForPackageStateChanges method [Windows Shell],IPackageDebugSettings interface, shell.IPackageDebugSettings_UnregisterForPackageStateChanges, shobjidl_core/IPackageDebugSettings::UnregisterForPackageStateChanges
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
 - IPackageDebugSettings::UnregisterForPackageStateChanges
 - shobjidl_core/IPackageDebugSettings::UnregisterForPackageStateChanges
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
 - IPackageDebugSettings.UnregisterForPackageStateChanges
---

# IPackageDebugSettings::UnregisterForPackageStateChanges


## -description

Stops receiving package state-change notifications associated with a previous call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-registerforpackagestatechanges">RegisterForPackageStateChanges</a>.

## -parameters

### -param dwCookie [in]

The notification to cancel. This identifier is returned by a previous call to the  <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-registerforpackagestatechanges">RegisterForPackageStateChanges</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call the <b>UnregisterForPackageStateChanges</b> to stop receiving package state-change notifications associated with a previous call to the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-registerforpackagestatechanges">RegisterForPackageStateChanges</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackagedebugsettings">IPackageDebugSettings</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-registerforpackagestatechanges">RegisterForPackageStateChanges</a>