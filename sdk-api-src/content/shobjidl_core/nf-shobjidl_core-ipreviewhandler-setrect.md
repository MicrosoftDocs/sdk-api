---
UID: NF:shobjidl_core.IPreviewHandler.SetRect
title: IPreviewHandler::SetRect (shobjidl_core.h)
description: Directs the preview handler to change the area within the parent hwnd that it draws into.
helpviewer_keywords: ["IPreviewHandler interface [Windows Shell]","SetRect method","IPreviewHandler.SetRect","IPreviewHandler::SetRect","SetRect","SetRect method [Windows Shell]","SetRect method [Windows Shell]","IPreviewHandler interface","_shell_IPreviewHandler_SetRect","shell.IPreviewHandler_SetRect","shobjidl_core/IPreviewHandler::SetRect"]
old-location: shell\IPreviewHandler_SetRect.htm
tech.root: shell
ms.assetid: 03353962-6905-4b13-bf7a-f1767767a7df
ms.date: 12/05/2018
ms.keywords: IPreviewHandler interface [Windows Shell],SetRect method, IPreviewHandler.SetRect, IPreviewHandler::SetRect, SetRect, SetRect method [Windows Shell], SetRect method [Windows Shell],IPreviewHandler interface, _shell_IPreviewHandler_SetRect, shell.IPreviewHandler_SetRect, shobjidl_core/IPreviewHandler::SetRect
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
 - IPreviewHandler::SetRect
 - shobjidl_core/IPreviewHandler::SetRect
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
 - IPreviewHandler.SetRect
---

# IPreviewHandler::SetRect


## -description

Directs the preview handler to change the area within the parent hwnd that it draws into.

## -parameters

### -param prc [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <b>RECT</b> to be used for the preview.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If called before the preview handler window has been created, the new <b>RECT</b>  replaces the <b>RECT</b> previously received in the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow">IPreviewHandler::SetWindow</a> call.

If called after the preview handler window has been created, the preview handler window must be resized.

If the preview handler is already rendering, then the preview must be resized without interrupting the render process.