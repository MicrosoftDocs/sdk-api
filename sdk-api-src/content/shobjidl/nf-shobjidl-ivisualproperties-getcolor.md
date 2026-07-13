---
UID: NF:shobjidl.IVisualProperties.GetColor
title: IVisualProperties::GetColor (shobjidl.h)
description: Gets the color, as specified.
helpviewer_keywords: ["GetColor","GetColor method [Windows Shell]","GetColor method [Windows Shell]","IVisualProperties interface","IVisualProperties interface [Windows Shell]","GetColor method","IVisualProperties.GetColor","IVisualProperties::GetColor","_shell_IVisualProperties_GetColor","shell.IVisualProperties_GetColor","shobjidl/IVisualProperties::GetColor"]
old-location: shell\IVisualProperties_GetColor.htm
tech.root: shell
ms.assetid: 538ac798-7722-434f-88bd-a7655d4c470c
ms.date: 12/05/2018
ms.keywords: GetColor, GetColor method [Windows Shell], GetColor method [Windows Shell],IVisualProperties interface, IVisualProperties interface [Windows Shell],GetColor method, IVisualProperties.GetColor, IVisualProperties::GetColor, _shell_IVisualProperties_GetColor, shell.IVisualProperties_GetColor, shobjidl/IVisualProperties::GetColor
req.header: shobjidl.h
req.include-header: 
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
 - IVisualProperties::GetColor
 - shobjidl/IVisualProperties::GetColor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IVisualProperties.GetColor
---

# IVisualProperties::GetColor


## -description

Gets the color, as specified.

## -parameters

### -param vpcf [in]

Type: <b><a href="/windows/desktop/api/shobjidl/ne-shobjidl-vpcolorflags">VPCOLORFLAGS</a></b>

The color flags. See <a href="/windows/desktop/api/shobjidl/ne-shobjidl-vpcolorflags">VPCOLORFLAGS</a>

### -param pcr [out]

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a>*</b>

A pointer to a value of type <a href="/windows/desktop/gdi/colorref">COLORREF</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.