---
UID: NF:shobjidl_core.IShellItemResources.SetTimes
title: IShellItemResources::SetTimes
author: windows-sdk-content
description: Sets file times.
old-location: shell\IShellItemResources_SetTimes.htm
tech.root: shell
ms.assetid: d5112da8-36a0-4b13-b674-c68eab24266d
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IShellItemResources interface [Windows Shell],SetTimes method, IShellItemResources.SetTimes, IShellItemResources::SetTimes, SetTimes, SetTimes method [Windows Shell], SetTimes method [Windows Shell],IShellItemResources interface, _shell_IShellItemResources_SetTimes, shell.IShellItemResources_SetTimes, shobjidl_core/IShellItemResources::SetTimes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - shobjidl_core.h
api_name:
 - IShellItemResources.SetTimes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shobjidl_core.h
: 
- IShellItemResources.SetTimes
: 
---

# IShellItemResources::SetTimes


## -description


Sets file times.


## -parameters




### -param pftCreation [in]

Type: <b>const FILETIME*</b>

A pointer to a creation date and time as a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


### -param pftWrite [in]

Type: <b>const FILETIME*</b>

A pointer to a write date and time as a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


### -param pftAccess [in]

Type: <b>const FILETIME*</b>

A pointer to an access date and time as a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



