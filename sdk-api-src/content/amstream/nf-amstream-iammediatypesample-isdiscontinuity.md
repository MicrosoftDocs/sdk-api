---
UID: NF:amstream.IAMMediaTypeSample.IsDiscontinuity
title: IAMMediaTypeSample::IsDiscontinuity (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The IsDiscontinuity method determines if this sample represents a discontinuity in the data stream.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","IsDiscontinuity method","IAMMediaTypeSample.IsDiscontinuity","IAMMediaTypeSample::IsDiscontinuity","IAMMediaTypeSampleIsDiscontinuity","IsDiscontinuity","IsDiscontinuity method [DirectShow]","IsDiscontinuity method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::IsDiscontinuity","dshow.iammediatypesample_isdiscontinuity"]
old-location: dshow\iammediatypesample_isdiscontinuity.htm
tech.root: dshow
ms.assetid: 857729d9-ef46-461b-a3b5-bce9acb84538
ms.date: 12/05/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],IsDiscontinuity method, IAMMediaTypeSample.IsDiscontinuity, IAMMediaTypeSample::IsDiscontinuity, IAMMediaTypeSampleIsDiscontinuity, IsDiscontinuity, IsDiscontinuity method [DirectShow], IsDiscontinuity method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::IsDiscontinuity, dshow.iammediatypesample_isdiscontinuity
req.header: amstream.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMMediaTypeSample::IsDiscontinuity
 - amstream/IAMMediaTypeSample::IsDiscontinuity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeSample.IsDiscontinuity
---

# IAMMediaTypeSample::IsDiscontinuity


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IsDiscontinuity</code> method determines if this sample represents a discontinuity in the data stream.



## -returns

Returns S_OK if this sample is a discontinuity, or S_FALSE otherwise.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>
