---
UID: NF:mixerocx.IMixerOCXNotify.OnInvalidateRect
title: IMixerOCXNotify::OnInvalidateRect (mixerocx.h)
author: windows-sdk-content
description: The OnInvalidateRect method notifies the client that the video rectangle has been invalidated.
old-location: dshow\imixerocxnotify_oninvalidaterect.htm
tech.root: DirectShow
ms.assetid: 55d349d4-1a9a-4762-8058-c3f7a559e272
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMixerOCXNotify interface [DirectShow],OnInvalidateRect method, IMixerOCXNotify.OnInvalidateRect, IMixerOCXNotify::OnInvalidateRect, IMixerOCXNotifyOnInvalidateRect, OnInvalidateRect, OnInvalidateRect method [DirectShow], OnInvalidateRect method [DirectShow],IMixerOCXNotify interface, dshow.imixerocxnotify_oninvalidaterect, mixerocx/IMixerOCXNotify::OnInvalidateRect
ms.topic: method
req.header: mixerocx.h
req.include-header: 
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
 - IMixerOCXNotify.OnInvalidateRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMixerOCXNotify::OnInvalidateRect


## -description



The <code>OnInvalidateRect</code> method notifies the client that the video rectangle has been invalidated.




## -parameters




### -param lpcRect [in]

Specifies the rectangle that has been invalidated, in screen coordinates.


## -returns



If the method succeeds, it returns S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mixerocx/nn-mixerocx-imixerocx">IMixerOCX Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mixerocx/nn-mixerocx-imixerocxnotify">IMixerOCXNotify Interface</a>
 

 

