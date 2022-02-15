---
UID: NF:shobjidl_core.IPackageExecutionStateChangeNotification.OnStateChanged
title: IPackageExecutionStateChangeNotification::OnStateChanged (shobjidl_core.h)
description: Called when package state changes during Windows Store app debugging.
helpviewer_keywords: ["IPackageExecutionStateChangeNotification interface [Windows Shell]","OnStateChanged method","IPackageExecutionStateChangeNotification.OnStateChanged","IPackageExecutionStateChangeNotification::OnStateChanged","OnStateChanged","OnStateChanged method [Windows Shell]","OnStateChanged method [Windows Shell]","IPackageExecutionStateChangeNotification interface","shell.IPackageExecutionStateChangeNotification_OnStateChanged","shobjidl_core/IPackageExecutionStateChangeNotification::OnStateChanged"]
old-location: shell\IPackageExecutionStateChangeNotification_OnStateChanged.htm
tech.root: shell
ms.assetid: 254986AF-4572-4D63-B055-1C05A8FB0417
ms.date: 12/05/2018
ms.keywords: IPackageExecutionStateChangeNotification interface [Windows Shell],OnStateChanged method, IPackageExecutionStateChangeNotification.OnStateChanged, IPackageExecutionStateChangeNotification::OnStateChanged, OnStateChanged, OnStateChanged method [Windows Shell], OnStateChanged method [Windows Shell],IPackageExecutionStateChangeNotification interface, shell.IPackageExecutionStateChangeNotification_OnStateChanged, shobjidl_core/IPackageExecutionStateChangeNotification::OnStateChanged
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - IPackageExecutionStateChangeNotification::OnStateChanged
 - shobjidl_core/IPackageExecutionStateChangeNotification::OnStateChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IPackageExecutionStateChangeNotification.OnStateChanged
---

# IPackageExecutionStateChangeNotification::OnStateChanged


## -description

Called when package state changes during Windows Store app debugging.

## -parameters

### -param pszPackageFullName [in]

The package full name.

### -param pesNewState [in]

The new state that the package changed to.

## -returns

Return <b>S_OK</b> when you implement the <b>OnStateChanged</b> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ipackageexecutionstatechangenotification">IPackageExecutionStateChangeNotification</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipackagedebugsettings-registerforpackagestatechanges">RegisterForPackageStateChanges</a>