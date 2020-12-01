---
UID: NF:amstream.IAMMediaTypeSample.GetPointer
title: IAMMediaTypeSample::GetPointer (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The GetPointer method retrieves a read/write pointer to the buffer's memory.
helpviewer_keywords: ["GetPointer","GetPointer method [DirectShow]","GetPointer method [DirectShow]","IAMMediaTypeSample interface","IAMMediaTypeSample interface [DirectShow]","GetPointer method","IAMMediaTypeSample.GetPointer","IAMMediaTypeSample::GetPointer","IAMMediaTypeSampleGetPointer","amstream/IAMMediaTypeSample::GetPointer","dshow.iammediatypesample_getpointer"]
old-location: dshow\iammediatypesample_getpointer.htm
tech.root: dshow
ms.assetid: e1ca46d8-51d6-4dd5-bbcc-463acf53420c
ms.date: 12/05/2018
ms.keywords: GetPointer, GetPointer method [DirectShow], GetPointer method [DirectShow],IAMMediaTypeSample interface, IAMMediaTypeSample interface [DirectShow],GetPointer method, IAMMediaTypeSample.GetPointer, IAMMediaTypeSample::GetPointer, IAMMediaTypeSampleGetPointer, amstream/IAMMediaTypeSample::GetPointer, dshow.iammediatypesample_getpointer
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
 - IAMMediaTypeSample::GetPointer
 - amstream/IAMMediaTypeSample::GetPointer
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
 - IAMMediaTypeSample.GetPointer
---

# IAMMediaTypeSample::GetPointer


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetPointer</code> method retrieves a read/write pointer to the buffer's memory.

## -parameters

### -param ppBuffer [out]

Address of a pointer to the buffer.

## -returns

Returns S_OK.

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>