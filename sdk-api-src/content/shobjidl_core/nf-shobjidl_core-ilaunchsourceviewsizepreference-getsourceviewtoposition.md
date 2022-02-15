---
UID: NF:shobjidl_core.ILaunchSourceViewSizePreference.GetSourceViewToPosition
title: ILaunchSourceViewSizePreference::GetSourceViewToPosition (shobjidl_core.h)
description: Retrieves the position of the source application window.
helpviewer_keywords: ["GetSourceViewToPosition","GetSourceViewToPosition method [Windows Shell]","GetSourceViewToPosition method [Windows Shell]","ILaunchSourceViewSizePreference interface","ILaunchSourceViewSizePreference interface [Windows Shell]","GetSourceViewToPosition method","ILaunchSourceViewSizePreference.GetSourceViewToPosition","ILaunchSourceViewSizePreference::GetSourceViewToPosition","shell.ILaunchSourceViewSizePreference_GetSourceViewToPosition","shobjidl_core/ILaunchSourceViewSizePreference::GetSourceViewToPosition"]
old-location: shell\ILaunchSourceViewSizePreference_GetSourceViewToPosition.htm
tech.root: shell
ms.assetid: 5B2D9CC9-D332-474E-A655-FBFC5E54AAE9
ms.date: 12/05/2018
ms.keywords: GetSourceViewToPosition, GetSourceViewToPosition method [Windows Shell], GetSourceViewToPosition method [Windows Shell],ILaunchSourceViewSizePreference interface, ILaunchSourceViewSizePreference interface [Windows Shell],GetSourceViewToPosition method, ILaunchSourceViewSizePreference.GetSourceViewToPosition, ILaunchSourceViewSizePreference::GetSourceViewToPosition, shell.ILaunchSourceViewSizePreference_GetSourceViewToPosition, shobjidl_core/ILaunchSourceViewSizePreference::GetSourceViewToPosition
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
 - ILaunchSourceViewSizePreference::GetSourceViewToPosition
 - shobjidl_core/ILaunchSourceViewSizePreference::GetSourceViewToPosition
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
 - ILaunchSourceViewSizePreference.GetSourceViewToPosition
---

# ILaunchSourceViewSizePreference::GetSourceViewToPosition


## -description

Retrieves the position of the source application window.

## -parameters

### -param hwnd [out]

Type: <b>HWND*</b>

Contains the address of a pointer to a window handle.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceviewsizepreference">ILaunchSourceViewSizePreference</a>