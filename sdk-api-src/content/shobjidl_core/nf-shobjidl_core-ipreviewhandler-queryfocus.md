---
UID: NF:shobjidl_core.IPreviewHandler.QueryFocus
title: IPreviewHandler::QueryFocus (shobjidl_core.h)
description: Directs the preview handler to return the HWND from calling the GetFocus Function.
helpviewer_keywords: ["IPreviewHandler interface [Windows Shell]","QueryFocus method","IPreviewHandler.QueryFocus","IPreviewHandler::QueryFocus","QueryFocus","QueryFocus method [Windows Shell]","QueryFocus method [Windows Shell]","IPreviewHandler interface","_shell_IPreviewHandler_QueryFocus","shell.IPreviewHandler_QueryFocus","shobjidl_core/IPreviewHandler::QueryFocus"]
old-location: shell\IPreviewHandler_QueryFocus.htm
tech.root: shell
ms.assetid: 8d21655b-ff0c-4396-a353-f968c28c4883
ms.date: 12/05/2018
ms.keywords: IPreviewHandler interface [Windows Shell],QueryFocus method, IPreviewHandler.QueryFocus, IPreviewHandler::QueryFocus, QueryFocus, QueryFocus method [Windows Shell], QueryFocus method [Windows Shell],IPreviewHandler interface, _shell_IPreviewHandler_QueryFocus, shell.IPreviewHandler_QueryFocus, shobjidl_core/IPreviewHandler::QueryFocus
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
 - IPreviewHandler::QueryFocus
 - shobjidl_core/IPreviewHandler::QueryFocus
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
 - IPreviewHandler.QueryFocus
---

# IPreviewHandler::QueryFocus


## -description

Directs the preview handler to return the <b>HWND</b> from calling the <a href="/windows/desktop/api/winuser/nf-winuser-getfocus">GetFocus Function</a>.

## -parameters

### -param phwnd [out]

Type: <b>HWND*</b>

When this method returns, contains a pointer to the HWND returned from calling the <a href="/windows/desktop/api/winuser/nf-winuser-getfocus">GetFocus Function</a> from the preview handler's foreground thread.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is necessary because <a href="/windows/desktop/api/winuser/nf-winuser-getfocus">GetFocus Function</a> can only succeed if the focus is on a window created by the calling thread. This method is used by the host to manage the tabbing order and to support tabbing into and out of the preview handler's windows.