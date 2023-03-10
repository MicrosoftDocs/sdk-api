---
UID: NF:shobjidl_core.IPreviewHandlerVisuals.SetTextColor
title: IPreviewHandlerVisuals::SetTextColor (shobjidl_core.h)
description: Sets the color of the text within the preview handler.
helpviewer_keywords: ["IPreviewHandlerVisuals interface [Windows Shell]","SetTextColor method","IPreviewHandlerVisuals.SetTextColor","IPreviewHandlerVisuals::SetTextColor","SetTextColor","SetTextColor method [Windows Shell]","SetTextColor method [Windows Shell]","IPreviewHandlerVisuals interface","_shell_IPreviewHandlerVisuals_SetTextColor","shell.IPreviewHandlerVisuals_SetTextColor","shobjidl_core/IPreviewHandlerVisuals::SetTextColor"]
old-location: shell\IPreviewHandlerVisuals_SetTextColor.htm
tech.root: shell
ms.assetid: 07278485-51a6-4729-8569-250478382a1e
ms.date: 12/05/2018
ms.keywords: IPreviewHandlerVisuals interface [Windows Shell],SetTextColor method, IPreviewHandlerVisuals.SetTextColor, IPreviewHandlerVisuals::SetTextColor, SetTextColor, SetTextColor method [Windows Shell], SetTextColor method [Windows Shell],IPreviewHandlerVisuals interface, _shell_IPreviewHandlerVisuals_SetTextColor, shell.IPreviewHandlerVisuals_SetTextColor, shobjidl_core/IPreviewHandlerVisuals::SetTextColor
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.redist: Windows Search 4 or later
ms.custom: 19H1
f1_keywords:
 - IPreviewHandlerVisuals::SetTextColor
 - shobjidl_core/IPreviewHandlerVisuals::SetTextColor
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
 - IPreviewHandlerVisuals.SetTextColor
---

# IPreviewHandlerVisuals::SetTextColor


## -description

Sets the color of the text within the preview handler.

## -parameters

### -param color [in]

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a></b>

A value of type <a href="/windows/desktop/gdi/colorref">COLORREF</a> to use for the preview handler text color.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Note</b>  These are suggestions. It is not compulsory for this method to be called; the preview handlers must be able to make their own decisions.</div>
<div> </div>