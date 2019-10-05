---
UID: NF:shobjidl_core.IPreviewHandlerFrame.TranslateAccelerator
title: IPreviewHandlerFrame::TranslateAccelerator (shobjidl_core.h)
author: windows-sdk-content
description: Directs the host to handle an keyboard shortcut passed from the preview handler.
old-location: shell\IPreviewHandlerFrame_TranslateAccelerator.htm
tech.root: shell
ms.assetid: 4f33a0b1-28ad-4e2d-9e2a-e58f44ab6f00
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPreviewHandlerFrame interface [Windows Shell],TranslateAccelerator method, IPreviewHandlerFrame.TranslateAccelerator, IPreviewHandlerFrame::TranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [Windows Shell], TranslateAccelerator method [Windows Shell],IPreviewHandlerFrame interface, _shell_IPreviewHandlerFrame_TranslateAccelerator, shell.IPreviewHandlerFrame_TranslateAccelerator, shobjidl_core/IPreviewHandlerFrame::TranslateAccelerator
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IPreviewHandlerFrame.TranslateAccelerator"
dev_langs:
 - c++
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
 - IPreviewHandlerFrame.TranslateAccelerator
targetos: Windows
req.typenames: 
req.redist: Windows Search 4 or later
ms.custom: 19H1
---

# IPreviewHandlerFrame::TranslateAccelerator


## -description


Directs the host to handle an keyboard shortcut passed from the preview handler.


## -parameters




### -param pmsg [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/menurc/wm-command">WM_COMMAND</a> or <a href="https://docs.microsoft.com/windows/desktop/menurc/wm-syscommand">WM_SYSCOMMAND</a> window message that corresponds to a keyboard shortcut.


## -returns



Type: <b>HRESULT</b>

If the keyboard shortcut is one that the host intends to handle, the host will process it and return <b>S_OK</b>; otherwise, it returns <b>S_FALSE</b>.




## -remarks



<div class="alert"><b>Note</b>  This method is only called by a preview handler in response to an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-translateaccelerator">TranslateAccelerator</a> call.</div>
<div> </div>


