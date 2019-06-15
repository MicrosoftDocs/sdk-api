---
UID: NF:amstream.IDirectDrawMediaSample.GetSurfaceAndReleaseLock
title: IDirectDrawMediaSample::GetSurfaceAndReleaseLock (amstream.h)
author: windows-sdk-content
description: The GetSurfaceAndReleaseLock method retrieves and unlocks the surface that the sample represents.
old-location: dshow\idirectdrawmediasample_getsurfaceandreleaselock.htm
tech.root: DirectShow
ms.assetid: f2b30974-ed4a-4783-bda5-9e7f4f9b4aab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSurfaceAndReleaseLock, GetSurfaceAndReleaseLock method [DirectShow], GetSurfaceAndReleaseLock method [DirectShow],IDirectDrawMediaSample interface, IDirectDrawMediaSample interface [DirectShow],GetSurfaceAndReleaseLock method, IDirectDrawMediaSample.GetSurfaceAndReleaseLock, IDirectDrawMediaSample::GetSurfaceAndReleaseLock, IDirectDrawMediaSampleGetSurfaceAndReleaseLock, amstream/IDirectDrawMediaSample::GetSurfaceAndReleaseLock, dshow.idirectdrawmediasample_getsurfaceandreleaselock
ms.topic: method
req.header: amstream.h
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
 - IDirectDrawMediaSample.GetSurfaceAndReleaseLock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawMediaSample::GetSurfaceAndReleaseLock


## -description



The <code>GetSurfaceAndReleaseLock</code> method retrieves and unlocks the surface that the sample represents.




## -parameters




### -param ppDirectDrawSurface [out]

Address of a pointer to the sample's <b>IDirectDrawSurface</b> interface.


### -param pRect [out]

Pointer to a variable that receives the address of the rectangle defining the part of the surface that the sample represents.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The caller should release the returned surface pointer, except when calling the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter's implementation of this interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nn-amstream-idirectdrawmediasample">IDirectDrawMediaSample Interface</a>
 

 

