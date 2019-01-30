---
UID: NF:strmif.IOverlayNotify.OnColorKeyChange
title: IOverlayNotify::OnColorKeyChange
author: windows-sdk-content
description: The OnColorKeyChange method provides notification that the window's color key has changed.
old-location: dshow\ioverlaynotify_oncolorkeychange.htm
tech.root: DirectShow
ms.assetid: a1e7fc88-a50a-4832-9b29-21b94184f1c7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IOverlayNotify interface [DirectShow],OnColorKeyChange method, IOverlayNotify.OnColorKeyChange, IOverlayNotify::OnColorKeyChange, IOverlayNotifyOnColorKeyChange, OnColorKeyChange, OnColorKeyChange method [DirectShow], OnColorKeyChange method [DirectShow],IOverlayNotify interface, dshow.ioverlaynotify_oncolorkeychange, strmif/IOverlayNotify::OnColorKeyChange
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IOverlayNotify.OnColorKeyChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOverlayNotify::OnColorKeyChange


## -description



The <code>OnColorKeyChange</code> method provides notification that the window's color key has changed.




## -parameters




### -param pColorKey [in]

Pointer to the new chroma key.


## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/77dcee49-35ef-4664-b0e6-3044352d543c">IOverlayNotify Interface</a>
 

 

