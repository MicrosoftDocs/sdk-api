---
UID: NF:strmif.IAMPushSource.GetMaxStreamOffset
title: IAMPushSource::GetMaxStreamOffset (strmif.h)
description: The GetMaxStreamOffset method retrieves the maximum stream offset the filter can support.
helpviewer_keywords: ["GetMaxStreamOffset","GetMaxStreamOffset method [DirectShow]","GetMaxStreamOffset method [DirectShow]","IAMPushSource interface","IAMPushSource interface [DirectShow]","GetMaxStreamOffset method","IAMPushSource.GetMaxStreamOffset","IAMPushSource::GetMaxStreamOffset","IAMPushSourceGetMaxStreamOffset","dshow.iampushsource_getmaxstreamoffset","strmif/IAMPushSource::GetMaxStreamOffset"]
old-location: dshow\iampushsource_getmaxstreamoffset.htm
tech.root: dshow
ms.assetid: 503ec642-0a86-47b9-b453-08ab90346630
ms.date: 12/05/2018
ms.keywords: GetMaxStreamOffset, GetMaxStreamOffset method [DirectShow], GetMaxStreamOffset method [DirectShow],IAMPushSource interface, IAMPushSource interface [DirectShow],GetMaxStreamOffset method, IAMPushSource.GetMaxStreamOffset, IAMPushSource::GetMaxStreamOffset, IAMPushSourceGetMaxStreamOffset, dshow.iampushsource_getmaxstreamoffset, strmif/IAMPushSource::GetMaxStreamOffset
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IAMPushSource::GetMaxStreamOffset
 - strmif/IAMPushSource::GetMaxStreamOffset
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
 - IAMPushSource.GetMaxStreamOffset
---

# IAMPushSource::GetMaxStreamOffset


## -description

The <code>GetMaxStreamOffset</code> method retrieves the maximum stream offset the filter can support.

## -parameters

### -param prtMaxOffset [out]

Pointer to a variable that receives a reference time indicating the maximum offset the filter can support.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation returns E_POINTER or S_OK.

## -remarks

If the stream offset is set to a value larger than the maximum supported offset, the filter is not guaranteed to have a buffer large enough to hold data for the entire amount of the offset. Unless there is another buffer downstream, data might be lost.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iampushsource">IAMPushSource Interface</a>