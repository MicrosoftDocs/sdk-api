---
UID: NF:shobjidl_core.IPreviewHandler.SetFocus
title: IPreviewHandler::SetFocus
author: windows-sdk-content
description: Directs the preview handler to set focus to itself.
old-location: shell\IPreviewHandler_SetFocus.htm
old-project: shell
ms.assetid: 93667383-da56-4fe9-a79e-933ab9703365
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IPreviewHandler interface [Windows Shell],SetFocus method, IPreviewHandler.SetFocus, IPreviewHandler::SetFocus, SetFocus, SetFocus method [Windows Shell], SetFocus method [Windows Shell],IPreviewHandler interface, _shell_IPreviewHandler_SetFocus, shell.IPreviewHandler_SetFocus, shobjidl_core/IPreviewHandler::SetFocus
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	IPreviewHandler.SetFocus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# IPreviewHandler::SetFocus


## -description


Directs the preview handler to set focus to itself.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method should query the state of the <b>SHIFT</b> key to decide whether to set focus to its first tab stop or its last tab stop. This is necessary because the <b>IPreviewHandler::SetFocus</b> can only succeed if the focus is being set to a window created by the calling thread.

This is the extent of accelerator keys coming down from the host to the preview handler; no other accelerators are passed down. <a href="https://msdn.microsoft.com/5e7e71f2-c728-44cb-820b-9a0b28b7266c">IPreviewHandler::TranslateAccelerator</a> is only used for messages from the preview handler's message pump up to the <a href="https://msdn.microsoft.com/a4e6507c-10b1-4c21-9359-92ba635a2a2c">IPreviewHandler</a> object.



