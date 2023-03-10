---
UID: NF:shobjidl_core.ILaunchTargetMonitor.GetMonitor
title: ILaunchTargetMonitor::GetMonitor (shobjidl_core.h)
description: Retrieves the target monitor for the application being launched.
helpviewer_keywords: ["GetMonitor","GetMonitor method [Windows Shell]","GetMonitor method [Windows Shell]","ILaunchTargetMonitor interface","ILaunchTargetMonitor interface [Windows Shell]","GetMonitor method","ILaunchTargetMonitor.GetMonitor","ILaunchTargetMonitor::GetMonitor","shell.ILaunchTargetMonitor_GetMonitor","shobjidl_core/ILaunchTargetMonitor::GetMonitor"]
old-location: shell\ILaunchTargetMonitor_GetMonitor.htm
tech.root: shell
ms.assetid: 88437C86-DC0F-42F4-B58E-E732E1DAB9FD
ms.date: 12/05/2018
ms.keywords: GetMonitor, GetMonitor method [Windows Shell], GetMonitor method [Windows Shell],ILaunchTargetMonitor interface, ILaunchTargetMonitor interface [Windows Shell],GetMonitor method, ILaunchTargetMonitor.GetMonitor, ILaunchTargetMonitor::GetMonitor, shell.ILaunchTargetMonitor_GetMonitor, shobjidl_core/ILaunchTargetMonitor::GetMonitor
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - ILaunchTargetMonitor::GetMonitor
 - shobjidl_core/ILaunchTargetMonitor::GetMonitor
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
 - ILaunchTargetMonitor.GetMonitor
---

# ILaunchTargetMonitor::GetMonitor


## -description

Retrieves the target monitor for the application being launched.

## -parameters

### -param monitor [out]

Type: <b>HMONITOR*</b>

Contains the address of a pointer to the target  monitor's handle.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetmonitor">ILaunchTargetMonitor</a>