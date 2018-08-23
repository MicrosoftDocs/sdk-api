---
UID: NF:amstream.IDirectDrawMediaSampleAllocator.GetDirectDraw
title: IDirectDrawMediaSampleAllocator::GetDirectDraw
author: windows-sdk-content
description: The GetDirectDraw method retrieves a pointer to the DirectDraw instance used to allocate surfaces.
old-location: dshow\idirectdrawmediasampleallocator_getdirectdraw.htm
old-project: DirectShow
ms.assetid: 6d6eed9d-635d-424b-ba14-213bbe56f66c
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: GetDirectDraw, GetDirectDraw method [DirectShow], GetDirectDraw method [DirectShow],IDirectDrawMediaSampleAllocator interface, IDirectDrawMediaSampleAllocator interface [DirectShow],GetDirectDraw method, IDirectDrawMediaSampleAllocator.GetDirectDraw, IDirectDrawMediaSampleAllocator::GetDirectDraw, IDirectDrawMediaSampleAllocatorGetDirectDraw, amstream/IDirectDrawMediaSampleAllocator::GetDirectDraw, dshow.idirectdrawmediasampleallocator_getdirectdraw
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: amstream.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: AMSI_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDirectDrawMediaSampleAllocator.GetDirectDraw
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IDirectDrawMediaSampleAllocator::GetDirectDraw


## -description



The <code>GetDirectDraw</code> method retrieves a pointer to the DirectDraw instance used to allocate surfaces.




## -parameters




### -param ppDirectDraw [out]

Address of a pointer that receives the DirectDraw object's <b>IDirectDraw</b> interface.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The caller should release the returned <b>IDirectDraw</b> pointer, except when calling the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter's implementation of this interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/35fd81ce-058a-4caf-b1de-f669be586f33">IDirectDrawMediaSampleAllocator Interface</a>
 

 

