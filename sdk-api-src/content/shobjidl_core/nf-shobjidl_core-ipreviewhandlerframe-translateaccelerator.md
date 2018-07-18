---
UID: NF:shobjidl_core.IPreviewHandlerFrame.TranslateAccelerator
title: IPreviewHandlerFrame::TranslateAccelerator
author: windows-sdk-content
description: Directs the host to handle an keyboard shortcut passed from the preview handler.
old-location: shell\IPreviewHandlerFrame_TranslateAccelerator.htm
old-project: shell
ms.assetid: 4f33a0b1-28ad-4e2d-9e2a-e58f44ab6f00
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IPreviewHandlerFrame interface [Windows Shell],TranslateAccelerator method, IPreviewHandlerFrame.TranslateAccelerator, IPreviewHandlerFrame::TranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [Windows Shell], TranslateAccelerator method [Windows Shell],IPreviewHandlerFrame interface, _shell_IPreviewHandlerFrame_TranslateAccelerator, shell.IPreviewHandlerFrame_TranslateAccelerator, shobjidl_core/IPreviewHandlerFrame::TranslateAccelerator
ms.prod: windows
ms.technology: windows-sdk
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
 - IPreviewHandlerFrame.TranslateAccelerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IPreviewHandlerFrame::TranslateAccelerator


## -description


Directs the host to handle an keyboard shortcut passed from the preview handler.


## -parameters




### -param pmsg [in]

Type: <b><a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/5516098e-fd90-49c8-afb0-78164b028376">WM_COMMAND</a> or <a href="https://msdn.microsoft.com/82c7cc95-82d5-4f0f-8c78-ab325561b04e">WM_SYSCOMMAND</a> window message that corresponds to a keyboard shortcut.


## -returns



Type: <b>HRESULT</b>

If the keyboard shortcut is one that the host intends to handle, the host will process it and return <b>S_OK</b>; otherwise, it returns <b>S_FALSE</b>.




## -remarks



<div class="alert"><b>Note</b>  This method is only called by a preview handler in response to an <a href="https://msdn.microsoft.com/5e7e71f2-c728-44cb-820b-9a0b28b7266c">TranslateAccelerator</a> call.</div>
<div> </div>


