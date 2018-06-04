---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



