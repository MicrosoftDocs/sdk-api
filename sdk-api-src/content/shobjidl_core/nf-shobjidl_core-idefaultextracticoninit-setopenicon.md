---
UID: NF:shobjidl_core.IDefaultExtractIconInit.SetOpenIcon
title: IDefaultExtractIconInit::SetOpenIcon (shobjidl_core.h)
description: Sets the icon that allows containers to specify an &quot;open&quot; look.
helpviewer_keywords: ["IDefaultExtractIconInit interface [Windows Shell]","SetOpenIcon method","IDefaultExtractIconInit.SetOpenIcon","IDefaultExtractIconInit::SetOpenIcon","SetOpenIcon","SetOpenIcon method [Windows Shell]","SetOpenIcon method [Windows Shell]","IDefaultExtractIconInit interface","_shell_IDefaultExtractIconInit_SetOpenIcon","shell.IDefaultExtractIconInit_SetOpenIcon","shobjidl_core/IDefaultExtractIconInit::SetOpenIcon"]
old-location: shell\IDefaultExtractIconInit_SetOpenIcon.htm
tech.root: shell
ms.assetid: 837a0006-2153-405f-a035-06738b89b058
ms.date: 12/05/2018
ms.keywords: IDefaultExtractIconInit interface [Windows Shell],SetOpenIcon method, IDefaultExtractIconInit.SetOpenIcon, IDefaultExtractIconInit::SetOpenIcon, SetOpenIcon, SetOpenIcon method [Windows Shell], SetOpenIcon method [Windows Shell],IDefaultExtractIconInit interface, _shell_IDefaultExtractIconInit_SetOpenIcon, shell.IDefaultExtractIconInit_SetOpenIcon, shobjidl_core/IDefaultExtractIconInit::SetOpenIcon
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
 - IDefaultExtractIconInit::SetOpenIcon
 - shobjidl_core/IDefaultExtractIconInit::SetOpenIcon
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
 - IDefaultExtractIconInit.SetOpenIcon
---

# IDefaultExtractIconInit::SetOpenIcon


## -description

Sets the icon that allows containers to specify an "open" look.

## -parameters

### -param pszFile [in, optional]

Type: <b>LPCWSTR</b>

A pointer to a buffer that contains the full icon path, including the file name and extension, as a Unicode string. This pointer can be <b>NULL</b>.

### -param iIcon

Type: <b>int</b>

Shell icon ID.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

