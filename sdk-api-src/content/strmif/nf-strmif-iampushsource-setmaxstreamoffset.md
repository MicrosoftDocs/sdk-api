---
UID: NF:strmif.IAMPushSource.SetMaxStreamOffset
title: IAMPushSource::SetMaxStreamOffset (strmif.h)
description: The SetMaxStreamOffset method specifies the stream offset that will be allowed in the filter graph.
helpviewer_keywords: ["IAMPushSource interface [DirectShow]","SetMaxStreamOffset method","IAMPushSource.SetMaxStreamOffset","IAMPushSource::SetMaxStreamOffset","IAMPushSourceSetMaxStreamOffset","SetMaxStreamOffset","SetMaxStreamOffset method [DirectShow]","SetMaxStreamOffset method [DirectShow]","IAMPushSource interface","dshow.iampushsource_setmaxstreamoffset","strmif/IAMPushSource::SetMaxStreamOffset"]
old-location: dshow\iampushsource_setmaxstreamoffset.htm
tech.root: dshow
ms.assetid: bbe0aa06-f680-4637-beb3-b94139ee0d54
ms.date: 12/05/2018
ms.keywords: IAMPushSource interface [DirectShow],SetMaxStreamOffset method, IAMPushSource.SetMaxStreamOffset, IAMPushSource::SetMaxStreamOffset, IAMPushSourceSetMaxStreamOffset, SetMaxStreamOffset, SetMaxStreamOffset method [DirectShow], SetMaxStreamOffset method [DirectShow],IAMPushSource interface, dshow.iampushsource_setmaxstreamoffset, strmif/IAMPushSource::SetMaxStreamOffset
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
 - IAMPushSource::SetMaxStreamOffset
 - strmif/IAMPushSource::SetMaxStreamOffset
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
 - IAMPushSource.SetMaxStreamOffset
---

# IAMPushSource::SetMaxStreamOffset


## -description

The <code>SetMaxStreamOffset</code> method specifies the stream offset that will be allowed in the filter graph.

## -parameters

### -param rtMaxOffset [in]

Reference time specifying the maximum stream offset.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -remarks

If this method is called prior to connecting the filter, the filter can allocate an appropriately sized buffer.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iampushsource">IAMPushSource Interface</a>