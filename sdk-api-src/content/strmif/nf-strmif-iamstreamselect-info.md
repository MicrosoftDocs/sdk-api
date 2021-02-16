---
UID: NF:strmif.IAMStreamSelect.Info
title: IAMStreamSelect::Info (strmif.h)
description: The Info method retrieves information about a given stream.
helpviewer_keywords: ["IAMStreamSelect interface [DirectShow]","Info method","IAMStreamSelect.Info","IAMStreamSelect::Info","IAMStreamSelectInfo","Info","Info method [DirectShow]","Info method [DirectShow]","IAMStreamSelect interface","dshow.iamstreamselect_info","strmif/IAMStreamSelect::Info"]
old-location: dshow\iamstreamselect_info.htm
tech.root: dshow
ms.assetid: 9396d4fb-e06e-4b54-9601-fd443c81ff35
ms.date: 12/05/2018
ms.keywords: IAMStreamSelect interface [DirectShow],Info method, IAMStreamSelect.Info, IAMStreamSelect::Info, IAMStreamSelectInfo, Info, Info method [DirectShow], Info method [DirectShow],IAMStreamSelect interface, dshow.iamstreamselect_info, strmif/IAMStreamSelect::Info
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
 - IAMStreamSelect::Info
 - strmif/IAMStreamSelect::Info
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
 - IAMStreamSelect.Info
---

# IAMStreamSelect::Info


## -description

The <code>Info</code> method retrieves information about a given stream.

## -parameters

### -param lIndex [in]

Zero-based index of the stream.

### -param ppmt [out]

Address of a variable that receives a pointer to the stream's media type. This parameter is optional and can be <b>NULL</b>. If the value is non-<b>NULL</b>, the method returns a pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure. The caller must delete the structure, including the format block. (You can use the <a href="/windows/desktop/DirectShow/deletemediatype">DeleteMediaType</a> function from the DirectShow base-class library.)

### -param pdwFlags [out]

Pointer to a variable that receives one of the following values:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>Zero</td>
<td>This stream is disabled.</td>
</tr>
<tr>
<td>AMSTREAMSELECTINFO_ENABLED</td>
<td>The stream is enabled, and others in this group might be enabled too.</td>
</tr>
<tr>
<td>AMSTREAMSELECTINFO_EXCLUSIVE</td>
<td>This stream is the only enabled stream in the group.</td>
</tr>
</table>
 

This parameter is optional and can be <b>NULL</b>.

### -param plcid [out]

Pointer to a variable that receives a locale context (LCID) value. If the stream is associated with a particular locale, the LCID is returned in this variable. Otherwise, the variable receives the value zero. This parameter is optional and can be <b>NULL</b>.

### -param pdwGroup [out]

Pointer to a variable that receives the logical group with which the stream is associated. This parameter is optional and can be <b>NULL</b>.

### -param ppszName [out]

Address of a variable that receives a pointer to the stream name. The caller must free the returned string by calling the <b>CoTaskMemFree</b> function. This parameter is optional and can be <b>NULL</b>.

### -param ppObject [out]

Address of a variable that receives an <b>IUnknown</b> interface pointer. The method might return a pointer to a pin or filter associated with the stream, or it might return the value <b>NULL</b>. If the method returns a non-<b>NULL</b> value, the caller must release the <b>IUnknown</b> pointer.

Calling the <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamselect-enable">IAMStreamSelect::Enable</a> method might invalidate the object returned by this method.

This parameter is optional and can be <b>NULL</b>.

The <a href="/windows/desktop/DirectShow/mpeg-1-stream-splitter-filter">MPEG-1 Stream Splitter</a>, <a href="/windows/desktop/DirectShow/mpeg-2-splitter">MPEG-2 Splitter</a>, and <a href="/windows/desktop/DirectShow/sami--cc--parser-filter">SAMI (CC) Parser</a> filters return a pointer to the pin associated with the selected stream.

### -param ppUnk [out]

Address of a variable that receives an <b>IUnknown</b> interface pointer. The method might return a pointer to an interface that is specific to the stream, or it might return the value <b>NULL</b>. If the method returns a non-<b>NULL</b> value, the caller must release the <b>IUnknown</b> pointer. This parameter is optional and can be <b>NULL</b>.

The MPEG-1 Stream Splitter, MPEG-2 Splitter, and SAMI (CC) Parser filters all return the value <b>NULL</b>. Third party filters might return a pointer to a custom filter interface.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The index is out of range.

</td>
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
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamstreamselect">IAMStreamSelect Interface</a>