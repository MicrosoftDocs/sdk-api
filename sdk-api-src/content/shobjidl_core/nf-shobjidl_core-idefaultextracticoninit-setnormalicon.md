---
UID: NF:shobjidl_core.IDefaultExtractIconInit.SetNormalIcon
title: IDefaultExtractIconInit::SetNormalIcon (shobjidl_core.h)
description: Sets the normal icon.
helpviewer_keywords: ["IDefaultExtractIconInit interface [Windows Shell]","SetNormalIcon method","IDefaultExtractIconInit.SetNormalIcon","IDefaultExtractIconInit::SetNormalIcon","SetNormalIcon","SetNormalIcon method [Windows Shell]","SetNormalIcon method [Windows Shell]","IDefaultExtractIconInit interface","_shell_IDefaultExtractIconInit_SetNormalIcon","shell.IDefaultExtractIconInit_SetNormalIcon","shobjidl_core/IDefaultExtractIconInit::SetNormalIcon"]
old-location: shell\IDefaultExtractIconInit_SetNormalIcon.htm
tech.root: shell
ms.assetid: 49d11767-4237-48f3-973b-03cf032c5e68
ms.date: 12/05/2018
ms.keywords: IDefaultExtractIconInit interface [Windows Shell],SetNormalIcon method, IDefaultExtractIconInit.SetNormalIcon, IDefaultExtractIconInit::SetNormalIcon, SetNormalIcon, SetNormalIcon method [Windows Shell], SetNormalIcon method [Windows Shell],IDefaultExtractIconInit interface, _shell_IDefaultExtractIconInit_SetNormalIcon, shell.IDefaultExtractIconInit_SetNormalIcon, shobjidl_core/IDefaultExtractIconInit::SetNormalIcon
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
 - IDefaultExtractIconInit::SetNormalIcon
 - shobjidl_core/IDefaultExtractIconInit::SetNormalIcon
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
 - IDefaultExtractIconInit.SetNormalIcon
---

# IDefaultExtractIconInit::SetNormalIcon


## -description

Sets the normal icon.

## -parameters

### -param pszFile [in, optional]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the full icon path, including the file name and extension, as a Unicode string. This pointer can be <b>NULL</b>.

### -param iIcon

Type: <b>int</b>

A Shell icon ID.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

