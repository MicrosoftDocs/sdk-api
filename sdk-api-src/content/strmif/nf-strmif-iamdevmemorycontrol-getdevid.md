---
UID: NF:strmif.IAMDevMemoryControl.GetDevId
title: IAMDevMemoryControl::GetDevId (strmif.h)
description: Note  The IAMDevMemoryControl interface is deprecated. Retrieves the device ID of the on-board memory allocator.
helpviewer_keywords: ["GetDevId","GetDevId method [DirectShow]","GetDevId method [DirectShow]","IAMDevMemoryControl interface","IAMDevMemoryControl interface [DirectShow]","GetDevId method","IAMDevMemoryControl.GetDevId","IAMDevMemoryControl::GetDevId","IAMDevMemoryControlGetDevId","dshow.iamdevmemorycontrol_getdevid","strmif/IAMDevMemoryControl::GetDevId"]
old-location: dshow\iamdevmemorycontrol_getdevid.htm
tech.root: dshow
ms.assetid: 398cc4b3-c025-4df4-8447-bd4599293dab
ms.date: 12/05/2018
ms.keywords: GetDevId, GetDevId method [DirectShow], GetDevId method [DirectShow],IAMDevMemoryControl interface, IAMDevMemoryControl interface [DirectShow],GetDevId method, IAMDevMemoryControl.GetDevId, IAMDevMemoryControl::GetDevId, IAMDevMemoryControlGetDevId, dshow.iamdevmemorycontrol_getdevid, strmif/IAMDevMemoryControl::GetDevId
req.header: strmif.h
req.include-header: Dshow.h
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
 - IAMDevMemoryControl::GetDevId
 - strmif/IAMDevMemoryControl::GetDevId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMDevMemoryControl.GetDevId
---

# IAMDevMemoryControl::GetDevId


## -description

<div class="alert"><b>Note</b>  The <b>IAMDevMemoryControl</b> interface is deprecated.</div>
<div> </div>
Retrieves the device ID of the on-board memory allocator.

## -parameters

### -param pdwDevId [out]

Pointer to the device ID.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

This method retrieves a unique ID that the hardware filter can use to verify that the specified allocator passed uses its on-board memory (because there can be more than one). The ID will be the same one as used to create the allocator object (using <b>CoCreateInstance</b>). For another filter to be able to use the on-board memory, it must have the same device ID as the on-board memory allocator.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamdevmemorycontrol">IAMDevMemoryControl Interface</a>