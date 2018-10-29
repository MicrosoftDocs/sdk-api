---
UID: NF:strmif.IOverlay.Unadvise
title: IOverlay::Unadvise
author: windows-sdk-content
description: The Unadvise method terminates the advise link established with the IOverlayNotify interface.
old-location: dshow\ioverlay_unadvise.htm
tech.root: DirectShow
ms.assetid: da987152-d5cd-42c5-848a-6d70ad25ca33
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IOverlay interface [DirectShow],Unadvise method, IOverlay.Unadvise, IOverlay::Unadvise, IOverlayUnadvise, Unadvise, Unadvise method [DirectShow], Unadvise method [DirectShow],IOverlay interface, dshow.ioverlay_unadvise, strmif/IOverlay::Unadvise
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IOverlay.Unadvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOverlay::Unadvise


## -description



The <code>Unadvise</code> method terminates the advise link established with the <a href="https://msdn.microsoft.com/77dcee49-35ef-4664-b0e6-3044352d543c">IOverlayNotify</a> interface.




## -parameters






## -returns



Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method terminates the advise link established by using the <a href="https://msdn.microsoft.com/02db2233-b185-47a9-9655-409991a74d4e">IOverlay::Advise</a> method. Only one advise link can be maintained at any one time.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay Interface</a>
 

 

