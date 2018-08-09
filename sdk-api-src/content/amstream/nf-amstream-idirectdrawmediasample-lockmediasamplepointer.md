---
UID: NF:amstream.IDirectDrawMediaSample.LockMediaSamplePointer
title: IDirectDrawMediaSample::LockMediaSamplePointer
author: windows-sdk-content
description: The LockMediaSamplePointer method locks the surface that the sample represents.
old-location: dshow\idirectdrawmediasample_lockmediasamplepointer.htm
old-project: DirectShow
ms.assetid: f711a82d-7560-43f8-8689-7f2fca77ae64
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IDirectDrawMediaSample interface [DirectShow],LockMediaSamplePointer method, IDirectDrawMediaSample.LockMediaSamplePointer, IDirectDrawMediaSample::LockMediaSamplePointer, IDirectDrawMediaSampleLockMediaSamplePointer, LockMediaSamplePointer, LockMediaSamplePointer method [DirectShow], LockMediaSamplePointer method [DirectShow],IDirectDrawMediaSample interface, amstream/IDirectDrawMediaSample::LockMediaSamplePointer, dshow.idirectdrawmediasample_lockmediasamplepointer
ms.prod: windows
ms.technology: windows-sdk
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
 - IDirectDrawMediaSample.LockMediaSamplePointer
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IDirectDrawMediaSample::LockMediaSamplePointer


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
 

 

