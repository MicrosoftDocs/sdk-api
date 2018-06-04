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

# IPreviewHandlerFrame::GetWindowContext


## -description


Gets a list of the keyboard shortcuts for the preview host.


## -parameters




### -param pinfo [out]

Type: <b><a href="https://msdn.microsoft.com/dd93675e-fd69-4fa3-a8e7-5238c27783d8">PREVIEWHANDLERFRAMEINFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/dd93675e-fd69-4fa3-a8e7-5238c27783d8">PREVIEWHANDLERFRAMEINFO</a> structure that receives accelerator table information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



An accelerator table is a list of keyboard shortcuts and the commands that the host should execute. As an optimization, the preview handler can then look at the keystrokes it receives, check them against the accelerator table to see if the host is interested in them, and forward them on if appropriate, ignoring the commands in the structure. The accelerator table returned from <b>IPreviewHandlerFrame::GetWindowContext</b>, contains only keystrokes and does not contain valid command entries. Preview handlers can also skip this optimization and simply call <a href="https://msdn.microsoft.com/4f33a0b1-28ad-4e2d-9e2a-e58f44ab6f00">IPreviewHandlerFrame::TranslateAccelerator</a> for every keystroke. When the preview handler is destroyed, the accelerator table must be freed using the <a href="https://msdn.microsoft.com/17fd308f-c1ad-41aa-ae65-72e22a7500f3">DestroyAcceleratorTable</a> function.

This method should be called at the point when the preview handler has called <a href="https://msdn.microsoft.com/5e95b2a6-85b3-4899-9e23-54ed9e69e821">SetSite</a> and the results have been cached for later use by the preview handler. This method cannot be called by preview handlers running in low-integrity mode.  Those preview handlers must always call <a href="https://msdn.microsoft.com/4f33a0b1-28ad-4e2d-9e2a-e58f44ab6f00">IPreviewHandlerFrame::TranslateAccelerator</a> for every keystroke.




## -see-also




<a href="https://msdn.microsoft.com/4e1316e5-f736-4a9b-887b-ddc48a615c42">IPreviewHandlerFrame</a>



<a href="https://msdn.microsoft.com/4f33a0b1-28ad-4e2d-9e2a-e58f44ab6f00">IPreviewHandlerFrame::TranslateAccelerator</a>
 

 

