---
UID: NF:shobjidl_core.IPreviewHandler.SetRect
title: IPreviewHandler::SetRect
author: windows-sdk-content
description: Directs the preview handler to change the area within the parent hwnd that it draws into.
old-location: shell\IPreviewHandler_SetRect.htm
old-project: shell
ms.assetid: 03353962-6905-4b13-bf7a-f1767767a7df
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPreviewHandler interface [Windows Shell],SetRect method, IPreviewHandler.SetRect, IPreviewHandler::SetRect, SetRect, SetRect method [Windows Shell], SetRect method [Windows Shell],IPreviewHandler interface, _shell_IPreviewHandler_SetRect, shell.IPreviewHandler_SetRect, shobjidl_core/IPreviewHandler::SetRect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: Windows Search 4 or later
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IPreviewHandler.SetRect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IPreviewHandler::SetRect


## -description


Directs the preview handler to change the area within the parent hwnd that it draws into.


## -parameters




### -param prc [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

A pointer to a <b>RECT</b> to be used for the preview.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If called before the preview handler window has been created, the new <b>RECT</b>  replaces the <b>RECT</b> previously received in the <a href="https://msdn.microsoft.com/a323811a-8244-40a0-a6b2-68572639be5f">IPreviewHandler::SetWindow</a> call.

If called after the preview handler window has been created, the preview handler window must be resized.

If the preview handler is already rendering, then the preview must be resized without interrupting the render process.



