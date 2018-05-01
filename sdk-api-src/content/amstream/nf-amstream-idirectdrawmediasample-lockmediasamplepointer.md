---
UID: NF:amstream.IDirectDrawMediaSample.LockMediaSamplePointer
title: IDirectDrawMediaSample::LockMediaSamplePointer method
author: windows-driver-content
description: The LockMediaSamplePointer method locks the surface that the sample represents.
old-location: dshow\idirectdrawmediasample_lockmediasamplepointer.htm
old-project: DirectShow
ms.assetid: f711a82d-7560-43f8-8689-7f2fca77ae64
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IDirectDrawMediaSample, IDirectDrawMediaSample interface [DirectShow], LockMediaSamplePointer method, IDirectDrawMediaSample::LockMediaSamplePointer, IDirectDrawMediaSampleLockMediaSamplePointer, LockMediaSamplePointer method [DirectShow], LockMediaSamplePointer method [DirectShow], IDirectDrawMediaSample interface, LockMediaSamplePointer,IDirectDrawMediaSample.LockMediaSamplePointer, amstream/IDirectDrawMediaSample::LockMediaSamplePointer, dshow.idirectdrawmediasample_lockmediasamplepointer
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
-	IDirectDrawMediaSample.LockMediaSamplePointer
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IDirectDrawMediaSample::LockMediaSamplePointer method


## -description



The <code>LockMediaSamplePointer</code> method locks the surface that the sample represents.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Call this method only after calling <a href="https://msdn.microsoft.com/f2b30974-ed4a-4783-bda5-9e7f4f9b4aab">IDirectDrawMediaSample::GetSurfaceAndReleaseLock</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/0a83b257-e88f-4870-924c-56ddc325f17f">IDirectDrawMediaSample Interface</a>
 

 

