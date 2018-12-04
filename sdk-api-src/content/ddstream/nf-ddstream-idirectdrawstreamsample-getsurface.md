---
UID: NF:ddstream.IDirectDrawStreamSample.GetSurface
title: IDirectDrawStreamSample::GetSurface
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. Retrieves pointers to the current sample's DirectDraw surface and associated clipping rectangle.
old-location: dshow\idirectdrawstreamsample_getsurface.htm
tech.root: DirectShow
ms.assetid: c6802940-53e5-4458-a1eb-deddd807a18a
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetSurface, GetSurface method [DirectShow], GetSurface method [DirectShow],IDirectDrawStreamSample interface, IDirectDrawStreamSample interface [DirectShow],GetSurface method, IDirectDrawStreamSample.GetSurface, IDirectDrawStreamSample::GetSurface, IDirectDrawStreamSampleGetSurface, ddstream/IDirectDrawStreamSample::GetSurface, dshow.idirectdrawstreamsample_getsurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ddstream.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ddstream.h
api_name:
 - IDirectDrawStreamSample.GetSurface
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawStreamSample::GetSurface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves pointers to the current sample's DirectDraw surface and associated clipping rectangle.




## -parameters




### -param ppDirectDrawSurface [out]

Address of a pointer to an <b>IDirectDrawSurface</b> interface that specifies the sample's new surface. Set this parameter to <b>NULL</b> if you don't want to specify a new surface.


### -param pRect [out]

Pointer to a <b>RECT</b> structure that will contain the current sample's clipping rectangle. Set this parameter to <b>NULL</b> if you don't want to retrieve the clipping rectangle.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Both parameters are optional. All implementations of this interface must support <b>NULL</b> values as valid parameters. If you retrieve a surface pointer, this method increments its reference count, so you must release the reference.




## -see-also




<a href="https://msdn.microsoft.com/afc8ac84-4629-4c5d-b4b2-59c1eb1af35d">IDirectDrawStreamSample Interface</a>
 

 

