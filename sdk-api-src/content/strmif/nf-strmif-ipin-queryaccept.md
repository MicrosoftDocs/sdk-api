---
UID: NF:strmif.IPin.QueryAccept
title: IPin::QueryAccept (strmif.h)
description: The QueryAccept method determines whether the pin accepts a specified media type.
helpviewer_keywords: ["IPin interface [DirectShow]","QueryAccept method","IPin.QueryAccept","IPin::QueryAccept","IPinQueryAccept","QueryAccept","QueryAccept method [DirectShow]","QueryAccept method [DirectShow]","IPin interface","dshow.ipin_queryaccept","strmif/IPin::QueryAccept"]
old-location: dshow\ipin_queryaccept.htm
tech.root: dshow
ms.assetid: ed11eeef-464b-4a75-958b-2bc6dbc7af04
ms.date: 12/05/2018
ms.keywords: IPin interface [DirectShow],QueryAccept method, IPin.QueryAccept, IPin::QueryAccept, IPinQueryAccept, QueryAccept, QueryAccept method [DirectShow], QueryAccept method [DirectShow],IPin interface, dshow.ipin_queryaccept, strmif/IPin::QueryAccept
f1_keywords:
- strmif/IPin.QueryAccept
dev_langs:
- c++
req.header: strmif.h
req.include-header: Dshow.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IPin.QueryAccept
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPin::QueryAccept


## -description



The <code>QueryAccept</code> method determines whether the pin accepts a specified media type.




## -parameters




### -param pmt [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that specifies the media type.


## -returns



Returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The pin rejects the media type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The pin accepts the media type.

</td>
</tr>
</table>
 




## -remarks



A return value of S_OK indicates that the pin will accept the media type, either on the next sample, or after a pin reconnection. The implementation should take into account the current state of the filter, including connections on other pins, and any properties that can be set on the filter.

Any other return value, including S_FALSE, means that the pin rejects the media type. Therefore, test for S_OK explicitly; do not use the <b>SUCCEEDED</b> macro.

If the filter is running, a return value of S_OK is ambiguous. The pin might accept a format change on the next media sample, without reconnecting; or it might need to reconnect. If the pin supports the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ipinconnection">IPinConnection</a> interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ipinconnection-dynamicqueryaccept">IPinConnection::DynamicQueryAccept</a> method, which specifically tests whether the pin can accept the new type without reconnecting.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dynamic-format-changes">Dynamic Format Changes</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>
 

 

