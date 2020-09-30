---
UID: NF:strmif.IAMPushSource.GetStreamOffset
title: IAMPushSource::GetStreamOffset (strmif.h)
description: The GetStreamOffset method retrieves the offset that the filter uses when generating time stamps.
helpviewer_keywords: ["GetStreamOffset","GetStreamOffset method [DirectShow]","GetStreamOffset method [DirectShow]","IAMPushSource interface","IAMPushSource interface [DirectShow]","GetStreamOffset method","IAMPushSource.GetStreamOffset","IAMPushSource::GetStreamOffset","IAMPushSourceGetStreamOffset","dshow.iampushsource_getstreamoffset","strmif/IAMPushSource::GetStreamOffset"]
old-location: dshow\iampushsource_getstreamoffset.htm
tech.root: dshow
ms.assetid: 249d5262-e02d-4df7-a968-0680b64ab7d4
ms.date: 12/05/2018
ms.keywords: GetStreamOffset, GetStreamOffset method [DirectShow], GetStreamOffset method [DirectShow],IAMPushSource interface, IAMPushSource interface [DirectShow],GetStreamOffset method, IAMPushSource.GetStreamOffset, IAMPushSource::GetStreamOffset, IAMPushSourceGetStreamOffset, dshow.iampushsource_getstreamoffset, strmif/IAMPushSource::GetStreamOffset
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
 - IAMPushSource::GetStreamOffset
 - strmif/IAMPushSource::GetStreamOffset
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
 - IAMPushSource.GetStreamOffset
---

# IAMPushSource::GetStreamOffset


## -description

The <code>GetStreamOffset</code> method retrieves the offset that the filter uses when generating time stamps.

## -parameters

### -param prtOffset [out]

Pointer to a variable that receives a reference time indicating the current stream offset.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iampushsource">IAMPushSource Interface</a>