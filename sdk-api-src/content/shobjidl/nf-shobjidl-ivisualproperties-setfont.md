---
UID: NF:shobjidl.IVisualProperties.SetFont
title: IVisualProperties::SetFont (shobjidl.h)
description: Sets attributes of the font.
helpviewer_keywords: ["IVisualProperties interface [Windows Shell]","SetFont method","IVisualProperties.SetFont","IVisualProperties::SetFont","SetFont","SetFont method [Windows Shell]","SetFont method [Windows Shell]","IVisualProperties interface","_shell_IVisualProperties_SetFont","shell.IVisualProperties_SetFont","shobjidl/IVisualProperties::SetFont"]
old-location: shell\IVisualProperties_SetFont.htm
tech.root: shell
ms.assetid: ecdf8652-0e1c-47df-bd19-80390bdf6c7f
ms.date: 12/05/2018
ms.keywords: IVisualProperties interface [Windows Shell],SetFont method, IVisualProperties.SetFont, IVisualProperties::SetFont, SetFont, SetFont method [Windows Shell], SetFont method [Windows Shell],IVisualProperties interface, _shell_IVisualProperties_SetFont, shell.IVisualProperties_SetFont, shobjidl/IVisualProperties::SetFont
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
 - IVisualProperties::SetFont
 - shobjidl/IVisualProperties::SetFont
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
 - IVisualProperties.SetFont
---

# IVisualProperties::SetFont


## -description

Sets attributes of the font.

## -parameters

### -param plf [in]

Type: <b>const LOGFONTW*</b>

A pointer to a <a href="/windows/win32/api/dimm/ns-dimm-logfonta">LOGFONT</a> structure that contains the attributes to set.

### -param bRedraw [in]

Type: <b>BOOL</b>

<b>TRUE</b> if the item should be redrawn after the new attributes are set; otherwise <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

