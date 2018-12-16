---
UID: NF:amstream.IDirectDrawMediaSample.LockMediaSamplePointer
title: IDirectDrawMediaSample::LockMediaSamplePointer
author: windows-sdk-content
description: The LockMediaSamplePointer method locks the surface that the sample represents.
old-location: dshow\idirectdrawmediasample_lockmediasamplepointer.htm
tech.root: DirectShow
ms.assetid: f711a82d-7560-43f8-8689-7f2fca77ae64
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectDrawMediaSample interface [DirectShow],LockMediaSamplePointer method, IDirectDrawMediaSample.LockMediaSamplePointer, IDirectDrawMediaSample::LockMediaSamplePointer, IDirectDrawMediaSampleLockMediaSamplePointer, LockMediaSamplePointer, LockMediaSamplePointer method [DirectShow], LockMediaSamplePointer method [DirectShow],IDirectDrawMediaSample interface, amstream/IDirectDrawMediaSample::LockMediaSamplePointer, dshow.idirectdrawmediasample_lockmediasamplepointer
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
 - IDirectDrawMediaSample.LockMediaSamplePointer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawMediaSample::LockMediaSamplePointer


## -description



The <code>LockMediaSamplePointer</code> method locks the surface that the sample represents.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Call this method only after calling <a href="https://msdn.microsoft.com/en-us/library/Dd406804(v=VS.85).aspx">IDirectDrawMediaSample::GetSurfaceAndReleaseLock</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd406801(v=VS.85).aspx">IDirectDrawMediaSample Interface</a>
 

 

