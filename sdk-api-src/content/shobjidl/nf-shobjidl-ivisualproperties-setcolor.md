---
UID: NF:shobjidl.IVisualProperties.SetColor
title: IVisualProperties::SetColor (shobjidl.h)
description: Sets the color, as specified.
old-location: shell\IVisualProperties_SetColor.htm
tech.root: shell
ms.assetid: 24e351af-687d-454a-9f0a-e7c07175dbd3
ms.date: 12/05/2018
ms.keywords: IVisualProperties interface [Windows Shell],SetColor method, IVisualProperties.SetColor, IVisualProperties::SetColor, SetColor, SetColor method [Windows Shell], SetColor method [Windows Shell],IVisualProperties interface, _shell_IVisualProperties_SetColor, shell.IVisualProperties_SetColor, shobjidl/IVisualProperties::SetColor
ms.topic: method
f1_keywords:
- shobjidl/IVisualProperties.SetColor
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shobjidl.h
api_name:
- IVisualProperties.SetColor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVisualProperties::SetColor


## -description


Sets the color, as specified.


## -parameters




### -param vpcf [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/ne-shobjidl-vpcolorflags">VPCOLORFLAGS</a></b>

The color flags. See <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl/ne-shobjidl-vpcolorflags">VPCOLORFLAGS</a>.


### -param cr [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a></b>

A value of type <a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>



## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



