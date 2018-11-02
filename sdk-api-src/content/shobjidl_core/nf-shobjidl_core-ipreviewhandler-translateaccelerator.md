---
UID: NF:shobjidl_core.IPreviewHandler.TranslateAccelerator
title: IPreviewHandler::TranslateAccelerator
author: windows-sdk-content
description: Directs the preview handler to handle a keystroke passed up from the message pump of the process in which the preview handler is running.
old-location: shell\IPreviewHandler_TranslateAccelerator.htm
tech.root: shell
ms.assetid: 5e7e71f2-c728-44cb-820b-9a0b28b7266c
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IPreviewHandler interface [Windows Shell],TranslateAccelerator method, IPreviewHandler.TranslateAccelerator, IPreviewHandler::TranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [Windows Shell], TranslateAccelerator method [Windows Shell],IPreviewHandler interface, _shell_IPreviewHandler_TranslateAccelerator, shell.IPreviewHandler_TranslateAccelerator, shobjidl_core/IPreviewHandler::TranslateAccelerator
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
 - IPreviewHandler.TranslateAccelerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Search 4 or later
---

# IPreviewHandler::TranslateAccelerator


## -description


Directs the preview handler to handle a keystroke passed up from the message pump of the process in which the preview handler is running.


## -parameters




### -param pmsg [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms644958(v=VS.85).aspx">MSG</a>*</b>

A pointer to a window message.


## -returns



Type: <b>HRESULT</b>

If the keystroke message can be processed by the preview handler, the handler will process it and return <b>S_OK</b>.  If the preview handler cannot process the keystroke message, it will offer it to the host using <a href="https://msdn.microsoft.com/4f33a0b1-28ad-4e2d-9e2a-e58f44ab6f00">TranslateAccelerator</a>.  If the host processes the message, this method will return <b>S_OK</b>.  If the host does not process the message, this method will return <b>S_FALSE</b>.




## -remarks



This function will only be called from the message pump of the process in which the preview handler is running. This function allows forwarding keystroke messages from the message pump to the host using <a href="https://msdn.microsoft.com/4f33a0b1-28ad-4e2d-9e2a-e58f44ab6f00">TranslateAccelerator</a>.

When the preview handler receives a message (a keystroke) from its message pump, it is responsible for forwarding it to its host.

When <a href="https://msdn.microsoft.com/5e95b2a6-85b3-4899-9e23-54ed9e69e821">IObjectWithSite::SetSite</a> is called on the preview handler, a reference to the preview handler's host is passed in.  The object should immediately <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> that site for <a href="https://msdn.microsoft.com/4e1316e5-f736-4a9b-887b-ddc48a615c42">IPreviewHandlerFrame</a>, and store that pointer.

The preview handler then has the option to call <a href="https://msdn.microsoft.com/953b7571-0da1-4e31-bb6f-1761f8103c6e">GetWindowContext</a> to get an accelerator table to filter keystrokes. The preview can then compare keystrokes against that accelerator table using <a href="https://msdn.microsoft.com/2d09f81a-b422-4379-89c8-d50992ebb24c">IsAccelerator</a> and only call <b>IPreviewHandler::TranslateAccelerator</b> for keystrokes that match.  This can cause a modest performance increase.  The preview handler must release the accelerator table using <a href="https://msdn.microsoft.com/en-us/library/ms646368(v=VS.85).aspx">DestroyAcceleratorTable</a> function.

It is also acceptable for the preview handler to avoid using the table altogether and call <b>IPreviewHandler::TranslateAccelerator</b> for every keystroke. Note that all preview handlers running in low-integrity processes must use this method.

When a tab key is pressed, if a preview handler has more than one tab stop it is responsible for moving keyboard focus within those tab stops.  If the current keyboard focus is on one of those tab stops, and advancing the keyboard focus would move it to another previewer tab stop, the previewer should call SetFocus on the next tab stop.  Otherwise the tab key should be forwarded to the host to handle tabbing out of the previewer.



