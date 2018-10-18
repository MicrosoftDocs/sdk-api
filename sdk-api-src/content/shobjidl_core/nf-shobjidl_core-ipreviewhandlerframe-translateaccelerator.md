---
UID: NF:shobjidl_core.IPreviewHandlerFrame.TranslateAccelerator
title: IPreviewHandlerFrame::TranslateAccelerator
author: windows-sdk-content
description: Directs the host to handle an keyboard shortcut passed from the preview handler.
old-location: shell\IPreviewHandlerFrame_TranslateAccelerator.htm
tech.root: shell
ms.assetid: 4f33a0b1-28ad-4e2d-9e2a-e58f44ab6f00
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: IPreviewHandlerFrame interface [Windows Shell],TranslateAccelerator method, IPreviewHandlerFrame.TranslateAccelerator, IPreviewHandlerFrame::TranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [Windows Shell], TranslateAccelerator method [Windows Shell],IPreviewHandlerFrame interface, _shell_IPreviewHandlerFrame_TranslateAccelerator, shell.IPreviewHandlerFrame_TranslateAccelerator, shobjidl_core/IPreviewHandlerFrame::TranslateAccelerator
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPreviewHandlerFrame.TranslateAccelerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Search 4 or later
---

# IPreviewHandlerFrame::TranslateAccelerator


## -description


Directs the host to handle an keyboard shortcut passed from the preview handler.


## -parameters




### -param pmsg [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms647591(v=VS.85).aspx">WM_COMMAND</a> or <a href="https://msdn.microsoft.com/en-us/library/ms646360(v=VS.85).aspx">WM_SYSCOMMAND</a> window message that corresponds to a keyboard shortcut.


## -returns



Type: <b>HRESULT</b>

If the keyboard shortcut is one that the host intends to handle, the host will process it and return <b>S_OK</b>; otherwise, it returns <b>S_FALSE</b>.




## -remarks



<div class="alert"><b>Note</b>  This method is only called by a preview handler in response to an <a href="https://msdn.microsoft.com/5e7e71f2-c728-44cb-820b-9a0b28b7266c">TranslateAccelerator</a> call.</div>
<div> </div>


