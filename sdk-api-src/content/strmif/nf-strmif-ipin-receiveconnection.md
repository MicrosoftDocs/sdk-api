---
UID: NF:strmif.IPin.ReceiveConnection
title: IPin::ReceiveConnection (strmif.h)
description: The ReceiveConnection method accepts a connection from another pin.
helpviewer_keywords: ["IPin interface [DirectShow]","ReceiveConnection method","IPin.ReceiveConnection","IPin::ReceiveConnection","IPinReceiveConnection","ReceiveConnection","ReceiveConnection method [DirectShow]","ReceiveConnection method [DirectShow]","IPin interface","dshow.ipin_receiveconnection","strmif/IPin::ReceiveConnection"]
old-location: dshow\ipin_receiveconnection.htm
tech.root: dshow
ms.assetid: b2013e95-88bc-4f4a-87af-2b13c120ec46
ms.date: 12/05/2018
ms.keywords: IPin interface [DirectShow],ReceiveConnection method, IPin.ReceiveConnection, IPin::ReceiveConnection, IPinReceiveConnection, ReceiveConnection, ReceiveConnection method [DirectShow], ReceiveConnection method [DirectShow],IPin interface, dshow.ipin_receiveconnection, strmif/IPin::ReceiveConnection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPin::ReceiveConnection
 - strmif/IPin::ReceiveConnection
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
 - IPin.ReceiveConnection
---

# IPin::ReceiveConnection


## -description

The <code>ReceiveConnection</code> method accepts a connection from another pin.



Applications should not call this method. This method is called by other filters during the pin connection process.

## -parameters

### -param pConnector [in]

Pointer to the connecting pin's <a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface.

### -param pmt [in]

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that specifies the media type for the connection.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_ALREADY_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is already connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
Cannot connect while filter is active.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_TYPE_NOT_ACCEPTED</b></dt>
</dl>
</td>
<td width="60%">
The specified media type is not acceptable.

</td>
</tr>
</table>

## -remarks

When an output pin connects, it calls this method on the input pin. The input pin should verify that the specified media type is acceptable. It may also need to check for other connection requirements specific to the owning filter. If the connection is suitable, the input pin should return S_OK, and also do the following:

<ul>
<li>Store the media type, and return the same type in the <a href="/windows/desktop/api/strmif/nf-strmif-ipin-connectionmediatype">IPin::ConnectionMediaType</a> method.</li>
<li>Store the output pin's <b>IPin</b> interface (<i>pConnector</i>), and return this pointer in the <a href="/windows/desktop/api/strmif/nf-strmif-ipin-connectedto">IPin::ConnectedTo</a> method.</li>
</ul>
If the connection is unsuitable, the pin should return an error code.

The <a href="/windows/desktop/DirectShow/cbasepin">CBasePin</a> class implements the basic framework for this method, including storing the media type and <b>IPin</b> pointers.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/DirectShow/how-filters-connect">How Filters Connect</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>