---
UID: NF:amstream.IDirectDrawMediaSample.LockMediaSamplePointer
title: IDirectDrawMediaSample::LockMediaSamplePointer (amstream.h)
description: The LockMediaSamplePointer method locks the surface that the sample represents.
helpviewer_keywords: ["IDirectDrawMediaSample interface [DirectShow]","LockMediaSamplePointer method","IDirectDrawMediaSample.LockMediaSamplePointer","IDirectDrawMediaSample::LockMediaSamplePointer","IDirectDrawMediaSampleLockMediaSamplePointer","LockMediaSamplePointer","LockMediaSamplePointer method [DirectShow]","LockMediaSamplePointer method [DirectShow]","IDirectDrawMediaSample interface","amstream/IDirectDrawMediaSample::LockMediaSamplePointer","dshow.idirectdrawmediasample_lockmediasamplepointer"]
old-location: dshow\idirectdrawmediasample_lockmediasamplepointer.htm
tech.root: dshow
ms.assetid: f711a82d-7560-43f8-8689-7f2fca77ae64
ms.date: 12/05/2018
ms.keywords: IDirectDrawMediaSample interface [DirectShow],LockMediaSamplePointer method, IDirectDrawMediaSample.LockMediaSamplePointer, IDirectDrawMediaSample::LockMediaSamplePointer, IDirectDrawMediaSampleLockMediaSamplePointer, LockMediaSamplePointer, LockMediaSamplePointer method [DirectShow], LockMediaSamplePointer method [DirectShow],IDirectDrawMediaSample interface, amstream/IDirectDrawMediaSample::LockMediaSamplePointer, dshow.idirectdrawmediasample_lockmediasamplepointer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectDrawMediaSample::LockMediaSamplePointer
 - amstream/IDirectDrawMediaSample::LockMediaSamplePointer
dev_langs:
 - c++
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
---

# IDirectDrawMediaSample::LockMediaSamplePointer


## -description

The <code>LockMediaSamplePointer</code> method locks the surface that the sample represents.



## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Call this method only after calling <a href="/windows/desktop/api/amstream/nf-amstream-idirectdrawmediasample-getsurfaceandreleaselock">IDirectDrawMediaSample::GetSurfaceAndReleaseLock</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amstream/nn-amstream-idirectdrawmediasample">IDirectDrawMediaSample Interface</a>
