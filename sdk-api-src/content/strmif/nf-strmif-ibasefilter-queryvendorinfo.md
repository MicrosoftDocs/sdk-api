---
UID: NF:strmif.IBaseFilter.QueryVendorInfo
title: IBaseFilter::QueryVendorInfo (strmif.h)
description: The QueryVendorInfo method retrieves a string containing vendor information.
helpviewer_keywords: ["IBaseFilter interface [DirectShow]","QueryVendorInfo method","IBaseFilter.QueryVendorInfo","IBaseFilter::QueryVendorInfo","IBaseFilterQueryVendorInfo","QueryVendorInfo","QueryVendorInfo method [DirectShow]","QueryVendorInfo method [DirectShow]","IBaseFilter interface","dshow.ibasefilter_queryvendorinfo","strmif/IBaseFilter::QueryVendorInfo"]
old-location: dshow\ibasefilter_queryvendorinfo.htm
tech.root: dshow
ms.assetid: 7524de26-360e-49c7-b636-7d05cf4d0ad2
ms.date: 12/05/2018
ms.keywords: IBaseFilter interface [DirectShow],QueryVendorInfo method, IBaseFilter.QueryVendorInfo, IBaseFilter::QueryVendorInfo, IBaseFilterQueryVendorInfo, QueryVendorInfo, QueryVendorInfo method [DirectShow], QueryVendorInfo method [DirectShow],IBaseFilter interface, dshow.ibasefilter_queryvendorinfo, strmif/IBaseFilter::QueryVendorInfo
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
 - IBaseFilter::QueryVendorInfo
 - strmif/IBaseFilter::QueryVendorInfo
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
 - IBaseFilter.QueryVendorInfo
---

# IBaseFilter::QueryVendorInfo


## -description

The <code>QueryVendorInfo</code> method retrieves a string containing vendor information.

## -parameters

### -param pVendorInfo [out]

Address of a variable that receives a pointer to a wide-character string containing the vendor information.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method is not supported.

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
</table>

## -remarks

This method is optional; filters are not required to support it.

If the method is supported, it uses the <b>CoTaskMemAlloc</b> function to allocate memory for the string. Call the <b>CoTaskMemFree</b> function to free the memory.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter Interface</a>