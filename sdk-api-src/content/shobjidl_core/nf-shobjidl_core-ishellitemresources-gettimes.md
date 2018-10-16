---
UID: NF:shobjidl_core.IShellItemResources.GetTimes
title: IShellItemResources::GetTimes
author: windows-sdk-content
description: Gets file times.
old-location: shell\IShellItemResources_GetTimes.htm
tech.root: shell
ms.assetid: 4857b824-2b58-4c26-bbab-8a799d20f584
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetTimes, GetTimes method [Windows Shell], GetTimes method [Windows Shell],IShellItemResources interface, IShellItemResources interface [Windows Shell],GetTimes method, IShellItemResources.GetTimes, IShellItemResources::GetTimes, _shell_IShellItemResources_GetTimes, shell.IShellItemResources_GetTimes, shobjidl_core/IShellItemResources::GetTimes
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
 - IShellItemResources.GetTimes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IShellItemResources::GetTimes


## -description


Gets file times.


## -parameters




### -param pftCreation [out]

Type: <b>FILETIME*</b>

A pointer to the creation date and time as a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


### -param pftWrite [out]

Type: <b>FILETIME*</b>

A pointer to write date and time as a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


### -param pftAccess [out]

Type: <b>FILETIME*</b>

A pointer to access date and time as a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



