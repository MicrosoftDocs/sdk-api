---
UID: NF:shobjidl_core.IExecuteCommandHost.GetUIMode
title: IExecuteCommandHost::GetUIMode (shobjidl_core.h)
description: Enables an IExplorerCommand-based Shell verb handler to query the UI mode of the host component from which the application was invoked..
helpviewer_keywords: ["ECHUIM_DESKTOP","ECHUIM_IMMERSIVE","ECHUIM_SYSTEM_LAUNCHER","GetUIMode","GetUIMode method [Windows Shell]","GetUIMode method [Windows Shell]","IExecuteCommandHost interface","IExecuteCommandHost interface [Windows Shell]","GetUIMode method","IExecuteCommandHost.GetUIMode","IExecuteCommandHost::GetUIMode","shell.IExecuteCommandHost_GetUIMode","shobjidl_core/IExecuteCommandHost::GetUIMode"]
old-location: shell\IExecuteCommandHost_GetUIMode.htm
tech.root: shell
ms.assetid: 12132ffd-64a5-4104-8590-8eabfbc8268f
ms.date: 12/05/2018
ms.keywords: ECHUIM_DESKTOP, ECHUIM_IMMERSIVE, ECHUIM_SYSTEM_LAUNCHER, GetUIMode, GetUIMode method [Windows Shell], GetUIMode method [Windows Shell],IExecuteCommandHost interface, IExecuteCommandHost interface [Windows Shell],GetUIMode method, IExecuteCommandHost.GetUIMode, IExecuteCommandHost::GetUIMode, shell.IExecuteCommandHost_GetUIMode, shobjidl_core/IExecuteCommandHost::GetUIMode
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
 - IExecuteCommandHost::GetUIMode
 - shobjidl_core/IExecuteCommandHost::GetUIMode
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
 - IExecuteCommandHost.GetUIMode
---

# IExecuteCommandHost::GetUIMode


## -description

Enables an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand">IExplorerCommand</a>-based Shell verb handler to query the UI mode of the host component from which the application was invoked.

## -parameters

### -param pUIMode [out]

Type: <b>EC_HOST_UI_MODE*</b>

#### ECHUIM_DESKTOP (0)

The application is running in the desktop environment.

#### ECHUIM_IMMERSIVE (1)

The application is running in the Windows 8 immersive environment.

#### ECHUIM_SYSTEM_LAUNCHER (2)

The application is running in the system launcher environment.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommandhost">IExecuteCommandHost</a>
