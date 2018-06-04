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

# IPreviewHandler::SetWindow


## -description


Sets the parent window of the previewer window, as well as the area within the parent to be used for the previewer window.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

A handle to the parent window.


### -param prc [in]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <b>RECT</b> defining the area for the previewer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The preview handler is responsible for painting the entire area defined by <i>prc</i>. If the previewer window has been created, the preview handler must associate the previewer window to the new parent <i>hwnd</i> and resize the previewer window to the area defined by <i>prc</i>. If the previewer window has not yet been created, the preview handler must remember this information for when the previewer window is created in <a href="https://msdn.microsoft.com/f6bad84f-9089-4905-ad4d-9b69ff9d11d6">IPreviewHandler::DoPreview</a>.

<div class="alert"><b>Note</b>  
            It is preferred that this information be stored prior to calling <a href="https://msdn.microsoft.com/f6bad84f-9089-4905-ad4d-9b69ff9d11d6">IPreviewHandler::DoPreview</a>. Doing so increases performance at setup time for any cases where the preview does not start.</div>
<div> </div>


