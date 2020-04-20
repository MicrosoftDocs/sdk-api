---
UID: NF:shobjidl_core.IDefaultExtractIconInit.SetDefaultIcon
title: IDefaultExtractIconInit::SetDefaultIcon (shobjidl_core.h)
description: Sets the default icon.helpviewer_keywords: ["IDefaultExtractIconInit interface [Windows Shell]","SetDefaultIcon method","IDefaultExtractIconInit.SetDefaultIcon","IDefaultExtractIconInit::SetDefaultIcon","SetDefaultIcon","SetDefaultIcon method [Windows Shell]","SetDefaultIcon method [Windows Shell]","IDefaultExtractIconInit interface","_shell_IDefaultExtractIconInit_SetDefaultIcon","shell.IDefaultExtractIconInit_SetDefaultIcon","shobjidl_core/IDefaultExtractIconInit::SetDefaultIcon"]
old-location: shell\IDefaultExtractIconInit_SetDefaultIcon.htm
tech.root: shell
ms.assetid: 7a834c1e-602a-4736-8807-7dd04c6dc5c2
ms.date: 12/05/2018
ms.keywords: IDefaultExtractIconInit interface [Windows Shell],SetDefaultIcon method, IDefaultExtractIconInit.SetDefaultIcon, IDefaultExtractIconInit::SetDefaultIcon, SetDefaultIcon, SetDefaultIcon method [Windows Shell], SetDefaultIcon method [Windows Shell],IDefaultExtractIconInit interface, _shell_IDefaultExtractIconInit_SetDefaultIcon, shell.IDefaultExtractIconInit_SetDefaultIcon, shobjidl_core/IDefaultExtractIconInit::SetDefaultIcon
f1_keywords:
- shobjidl_core/IDefaultExtractIconInit.SetDefaultIcon
dev_langs:
- c++
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
- IDefaultExtractIconInit.SetDefaultIcon
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDefaultExtractIconInit::SetDefaultIcon


## -description


Sets the default icon.


## -parameters




### -param pszFile [in, optional]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the full icon path, including the file name and extension, as a Unicode string. This pointer can be <b>NULL</b>.


### -param iIcon

Type: <b>int</b>

The Shell icon ID.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



