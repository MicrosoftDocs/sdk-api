---
UID: NF:amstream.IAMMediaTypeSample.SetPreroll
title: IAMMediaTypeSample::SetPreroll (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetPreroll method specifies whether this is a preroll sample. A preroll sample should not be displayed.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","SetPreroll method","IAMMediaTypeSample.SetPreroll","IAMMediaTypeSample::SetPreroll","IAMMediaTypeSampleSetPreroll","SetPreroll","SetPreroll method [DirectShow]","SetPreroll method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::SetPreroll","dshow.iammediatypesample_setpreroll"]
old-location: dshow\iammediatypesample_setpreroll.htm
tech.root: dshow
ms.assetid: f4815f4f-b919-497a-922e-b4d0d2078e4b
ms.date: 12/05/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetPreroll method, IAMMediaTypeSample.SetPreroll, IAMMediaTypeSample::SetPreroll, IAMMediaTypeSampleSetPreroll, SetPreroll, SetPreroll method [DirectShow], SetPreroll method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetPreroll, dshow.iammediatypesample_setpreroll
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
 - IAMMediaTypeSample::SetPreroll
 - amstream/IAMMediaTypeSample::SetPreroll
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
 - IAMMediaTypeSample.SetPreroll
---

# IAMMediaTypeSample::SetPreroll


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetPreroll</code> method specifies whether this is a preroll sample. A preroll sample should not be displayed.

## -parameters

### -param bIsPreroll

Boolean value that specifies whether the sample is a preroll sample. If <b>TRUE</b>, it is for preroll and should not be displayed.

## -returns

Returns S_OK.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>