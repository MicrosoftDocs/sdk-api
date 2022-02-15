---
UID: NF:shobjidl_core.IDefaultExtractIconInit.SetFlags
title: IDefaultExtractIconInit::SetFlags (shobjidl_core.h)
description: Sets GIL_XXX flags.
helpviewer_keywords: ["IDefaultExtractIconInit interface [Windows Shell]","SetFlags method","IDefaultExtractIconInit.SetFlags","IDefaultExtractIconInit::SetFlags","SetFlags","SetFlags method [Windows Shell]","SetFlags method [Windows Shell]","IDefaultExtractIconInit interface","_shell_IDefaultExtractIconInit_SetFlags","shell.IDefaultExtractIconInit_SetFlags","shobjidl_core/IDefaultExtractIconInit::SetFlags"]
old-location: shell\IDefaultExtractIconInit_SetFlags.htm
tech.root: shell
ms.assetid: d16a7c14-c9b9-474b-82ce-0c8e890271b7
ms.date: 12/05/2018
ms.keywords: IDefaultExtractIconInit interface [Windows Shell],SetFlags method, IDefaultExtractIconInit.SetFlags, IDefaultExtractIconInit::SetFlags, SetFlags, SetFlags method [Windows Shell], SetFlags method [Windows Shell],IDefaultExtractIconInit interface, _shell_IDefaultExtractIconInit_SetFlags, shell.IDefaultExtractIconInit_SetFlags, shobjidl_core/IDefaultExtractIconInit::SetFlags
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
 - IDefaultExtractIconInit::SetFlags
 - shobjidl_core/IDefaultExtractIconInit::SetFlags
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
 - IDefaultExtractIconInit.SetFlags
---

# IDefaultExtractIconInit::SetFlags


## -description

Sets GIL_XXX flags. See <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation">GetIconLocation</a>

## -parameters

### -param uFlags [in]

Type: <b>UINT</b>

Specifies return flags to get icon location.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.