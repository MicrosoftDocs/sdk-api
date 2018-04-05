---
UID: NF:amstream.IDirectDrawMediaSample.GetSurfaceAndReleaseLock
title: IDirectDrawMediaSample::GetSurfaceAndReleaseLock method
author: windows-driver-content
description: The GetSurfaceAndReleaseLock method retrieves and unlocks the surface that the sample represents.
old-location: dshow\idirectdrawmediasample_getsurfaceandreleaselock.htm
old-project: DirectShow
ms.assetid: f2b30974-ed4a-4783-bda5-9e7f4f9b4aab
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetSurfaceAndReleaseLock method [DirectShow], GetSurfaceAndReleaseLock method [DirectShow], IDirectDrawMediaSample interface, GetSurfaceAndReleaseLock,IDirectDrawMediaSample.GetSurfaceAndReleaseLock, IDirectDrawMediaSample, IDirectDrawMediaSample interface [DirectShow], GetSurfaceAndReleaseLock method, IDirectDrawMediaSample::GetSurfaceAndReleaseLock, IDirectDrawMediaSampleGetSurfaceAndReleaseLock, amstream/IDirectDrawMediaSample::GetSurfaceAndReleaseLock, dshow.idirectdrawmediasample_getsurfaceandreleaselock
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AMSI_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDirectDrawMediaSample.GetSurfaceAndReleaseLock
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IDirectDrawMediaSample::GetSurfaceAndReleaseLock method


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



The caller should release the returned surface pointer, except when calling the <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter's implementation of this interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0a83b257-e88f-4870-924c-56ddc325f17f">IDirectDrawMediaSample Interface</a>
 

 

