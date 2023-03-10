---
UID: NF:strmif.IBaseFilter.EnumPins
title: IBaseFilter::EnumPins (strmif.h)
description: The EnumPins method enumerates the pins on this filter.
helpviewer_keywords: ["EnumPins","EnumPins method [DirectShow]","EnumPins method [DirectShow]","IBaseFilter interface","IBaseFilter interface [DirectShow]","EnumPins method","IBaseFilter.EnumPins","IBaseFilter::EnumPins","IBaseFilterEnumPins","dshow.ibasefilter_enumpins","strmif/IBaseFilter::EnumPins"]
old-location: dshow\ibasefilter_enumpins.htm
tech.root: dshow
ms.assetid: 02675c93-7901-40f6-a9fc-f6f13f56acca
ms.date: 12/05/2018
ms.keywords: EnumPins, EnumPins method [DirectShow], EnumPins method [DirectShow],IBaseFilter interface, IBaseFilter interface [DirectShow],EnumPins method, IBaseFilter.EnumPins, IBaseFilter::EnumPins, IBaseFilterEnumPins, dshow.ibasefilter_enumpins, strmif/IBaseFilter::EnumPins
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
 - IBaseFilter::EnumPins
 - strmif/IBaseFilter::EnumPins
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
 - IBaseFilter.EnumPins
---

# IBaseFilter::EnumPins


## -description

The <code>EnumPins</code> method enumerates the pins on this filter.

## -parameters

### -param ppEnum [out]

Address of a variable that receives a pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-ienumpins">IEnumPins</a> interface.

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
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
</table>

## -remarks

This method returns an enumerator that supports the <b>IEnumPins</b> interface, which works like a standard COM enumerator. For more information, see <a href="/windows/desktop/DirectShow/enumerating-pins">Enumerating Pins</a>.

If the method succeeds, the <b>IEnumPins</b> interface has an outstanding reference count. Be sure to release the interface when you are done.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter Interface</a>