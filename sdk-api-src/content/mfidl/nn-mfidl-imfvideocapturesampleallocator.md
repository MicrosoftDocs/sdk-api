---
UID: NN:mfidl.IMFVideoCaptureSampleAllocator
title: IMFVideoCaptureSampleAllocator
ms.date: 1/23/2020
targetos: Windows
description: Allocates video samples for a video media sink with specialized functionality for video capture devices.
tech.root: mf
req.assembly: mfuuid.dll
req.construct-type: iface
req.ddi-compliance: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFVideoCaptureSampleAllocator
f1_keywords:
 - IMFVideoCaptureSampleAllocator
 - mfidl/IMFVideoCaptureSampleAllocator
dev_langs:
 - c++
---

## -description

Allocates video samples for a video media sink with specialized functionality for video capture devices.

## -remarks

This interface inherits from [IMFVideoSampleAllocator](nn-mfidl-imfvideosampleallocator.md) and provides the [InitializeCaptureSampleAllocator](nf-mfidl-imfvideocapturesampleallocator-initializecapturesampleallocator.md) method with parameters relevant to video capture scenarios.

## -see-also

