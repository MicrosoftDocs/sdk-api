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

# IFrameworkInputPane::AdviseWithHWND


## -description


Registers the app's input pane handler object to receive notifications on behalf of a window when an event triggers the input pane. This method differs from <a href="https://msdn.microsoft.com/F05A097F-13A4-48ad-B660-5B2409BB6D61">Advise</a> in that it references its window through an <b>HWND</b>.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window for which the handler should listen for input pane events.


### -param pHandler [in]

Type: <b><a href="https://msdn.microsoft.com/E8038442-9E96-4eee-968E-3A6BC747852D">IFrameworkInputPaneHandler</a>*</b>

An <a href="https://msdn.microsoft.com/E8038442-9E96-4eee-968E-3A6BC747852D">IFrameworkInputPaneHandler</a> interface pointer to the handler instance for this app.


### -param pdwCookie [out]

Type: <b>DWORD*</b>

A pointer to a value that, when this method returns successfully, receives a cookie for that can be used later to unregister the handler through the <a href="https://msdn.microsoft.com/E4187EC2-DD8F-4e3c-BD0C-B5AD4B02E943">Unadvise</a> method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/05C115BA-249A-4271-9C6F-DAAEE91BB936">IFrameworkInputPane</a>



<a href="https://msdn.microsoft.com/F05A097F-13A4-48ad-B660-5B2409BB6D61">IFrameworkInputPane::Advise</a>



<a href="https://msdn.microsoft.com/E4187EC2-DD8F-4e3c-BD0C-B5AD4B02E943">IFrameworkInputPane::Unadvise</a>
 

 

