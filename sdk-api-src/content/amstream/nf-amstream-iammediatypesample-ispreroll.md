---
UID: NF:amstream.IAMMediaTypeSample.IsPreroll
title: IAMMediaTypeSample::IsPreroll (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The IsPreroll method determines if this sample is part of the preroll. A preroll sample should not be displayed.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","IsPreroll method","IAMMediaTypeSample.IsPreroll","IAMMediaTypeSample::IsPreroll","IAMMediaTypeSampleIsPreroll","IsPreroll","IsPreroll method [DirectShow]","IsPreroll method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::IsPreroll","dshow.iammediatypesample_ispreroll"]
old-location: dshow\iammediatypesample_ispreroll.htm
tech.root: dshow
ms.assetid: 57ae9d67-65b9-458e-ad94-f5d5c89d1984
ms.date: 12/05/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],IsPreroll method, IAMMediaTypeSample.IsPreroll, IAMMediaTypeSample::IsPreroll, IAMMediaTypeSampleIsPreroll, IsPreroll, IsPreroll method [DirectShow], IsPreroll method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::IsPreroll, dshow.iammediatypesample_ispreroll
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
 - IAMMediaTypeSample::IsPreroll
 - amstream/IAMMediaTypeSample::IsPreroll
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
 - IAMMediaTypeSample.IsPreroll
---

# IAMMediaTypeSample::IsPreroll


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IsPreroll</code> method determines if this sample is part of the preroll. A preroll sample should not be displayed.



## -returns

Returns S_OK if the sample is a preroll sample, or S_FALSE otherwise.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>
