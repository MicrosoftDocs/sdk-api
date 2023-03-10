---
UID: NF:shobjidl_core.IShellItemResources.GetTimes
title: IShellItemResources::GetTimes (shobjidl_core.h)
description: Gets file times.
helpviewer_keywords: ["GetTimes","GetTimes method [Windows Shell]","GetTimes method [Windows Shell]","IShellItemResources interface","IShellItemResources interface [Windows Shell]","GetTimes method","IShellItemResources.GetTimes","IShellItemResources::GetTimes","_shell_IShellItemResources_GetTimes","shell.IShellItemResources_GetTimes","shobjidl_core/IShellItemResources::GetTimes"]
old-location: shell\IShellItemResources_GetTimes.htm
tech.root: shell
ms.assetid: 4857b824-2b58-4c26-bbab-8a799d20f584
ms.date: 12/05/2018
ms.keywords: GetTimes, GetTimes method [Windows Shell], GetTimes method [Windows Shell],IShellItemResources interface, IShellItemResources interface [Windows Shell],GetTimes method, IShellItemResources.GetTimes, IShellItemResources::GetTimes, _shell_IShellItemResources_GetTimes, shell.IShellItemResources_GetTimes, shobjidl_core/IShellItemResources::GetTimes
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItemResources::GetTimes
 - shobjidl_core/IShellItemResources::GetTimes
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
 - IShellItemResources.GetTimes
---

# IShellItemResources::GetTimes


## -description

Gets file times.

## -parameters

### -param pftCreation [out]

Type: <b>FILETIME*</b>

A pointer to the creation date and time as a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

### -param pftWrite [out]

Type: <b>FILETIME*</b>

A pointer to write date and time as a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

### -param pftAccess [out]

Type: <b>FILETIME*</b>

A pointer to access date and time as a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.