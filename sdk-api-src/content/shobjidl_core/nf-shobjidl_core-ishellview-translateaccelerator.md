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

# IShellView::TranslateAccelerator


## -description


Translates keyboard shortcut (accelerator) key strokes when a namespace extension's view has the focus.


## -parameters




### -param pmsg






#### - lpmsg

Type: <b>LPMSG</b>

The address of the message to be translated.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

If the view returns S_OK, it indicates that the message was translated and should not be translated or dispatched by Windows Explorer.




## -remarks



This method is called by Windows Explorer to let the view translate its keyboard shortcuts.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
Windows Explorer calls this method before any other translation if the view has the focus. If the view does not have the focus, it is called after Windows Explorer translates its own keyboard shortcuts.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
By default, the view should return S_FALSE so that Windows Explorer can either do its own keyboard shortcut translation or normal menu dispatching. The view should return S_OK only if it has processed the message as the keyboard shortcut and does not want Windows Explorer to process it further.




## -see-also




<a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>
 

 

