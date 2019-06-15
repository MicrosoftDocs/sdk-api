---
UID: NF:shobjidl_core.IPreviewHandler.SetWindow
title: IPreviewHandler::SetWindow (shobjidl_core.h)
author: windows-sdk-content
description: Sets the parent window of the previewer window, as well as the area within the parent to be used for the previewer window.
old-location: shell\IPreviewHandler_SetWindow.htm
tech.root: shell
ms.assetid: a323811a-8244-40a0-a6b2-68572639be5f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPreviewHandler interface [Windows Shell],SetWindow method, IPreviewHandler.SetWindow, IPreviewHandler::SetWindow, SetWindow, SetWindow method [Windows Shell], SetWindow method [Windows Shell],IPreviewHandler interface, _shell_IPreviewHandler_SetWindow, shell.IPreviewHandler_SetWindow, shobjidl_core/IPreviewHandler::SetWindow
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IPreviewHandler.SetWindow
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Search 4 or later
ms.custom: 19H1
---

# IPreviewHandler::SetWindow


## -description


Sets the parent window of the previewer window, as well as the area within the parent to be used for the previewer window.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the parent window.


### -param prc [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <b>RECT</b> defining the area for the previewer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The preview handler is responsible for painting the entire area defined by <i>prc</i>. If the previewer window has been created, the preview handler must associate the previewer window to the new parent <i>hwnd</i> and resize the previewer window to the area defined by <i>prc</i>. If the previewer window has not yet been created, the preview handler must remember this information for when the previewer window is created in <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview">IPreviewHandler::DoPreview</a>.

<div class="alert"><b>Note</b>  It is preferred that this information be stored prior to calling <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview">IPreviewHandler::DoPreview</a>. Doing so increases performance at setup time for any cases where the preview does not start.</div>
<div> </div>


