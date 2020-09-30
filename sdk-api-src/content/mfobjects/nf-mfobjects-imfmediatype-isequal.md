---
UID: NF:mfobjects.IMFMediaType.IsEqual
title: IMFMediaType::IsEqual (mfobjects.h)
description: Compares two media types and determines whether they are identical. If they are not identical, the method indicates how the two formats differ.
helpviewer_keywords: ["42b5b0e8-3b13-4bda-a53c-0428a3c9b131","IMFMediaType interface [Media Foundation]","IsEqual method","IMFMediaType.IsEqual","IMFMediaType::IsEqual","IsEqual","IsEqual method [Media Foundation]","IsEqual method [Media Foundation]","IMFMediaType interface","MF_MEDIATYPE_EQUAL_FORMAT_DATA","MF_MEDIATYPE_EQUAL_FORMAT_TYPES","MF_MEDIATYPE_EQUAL_FORMAT_USER_DATA","MF_MEDIATYPE_EQUAL_MAJOR_TYPES","mf.imfmediatype_isequal","mfobjects/IMFMediaType::IsEqual"]
old-location: mf\imfmediatype_isequal.htm
tech.root: mf
ms.assetid: 42b5b0e8-3b13-4bda-a53c-0428a3c9b131
ms.date: 12/05/2018
ms.keywords: 42b5b0e8-3b13-4bda-a53c-0428a3c9b131, IMFMediaType interface [Media Foundation],IsEqual method, IMFMediaType.IsEqual, IMFMediaType::IsEqual, IsEqual, IsEqual method [Media Foundation], IsEqual method [Media Foundation],IMFMediaType interface, MF_MEDIATYPE_EQUAL_FORMAT_DATA, MF_MEDIATYPE_EQUAL_FORMAT_TYPES, MF_MEDIATYPE_EQUAL_FORMAT_USER_DATA, MF_MEDIATYPE_EQUAL_MAJOR_TYPES, mf.imfmediatype_isequal, mfobjects/IMFMediaType::IsEqual
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMediaType::IsEqual
 - mfobjects/IMFMediaType::IsEqual
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaType.IsEqual
---

# IMFMediaType::IsEqual


## -description

Compares two media types and determines whether they are identical. If they are not identical, the method indicates how the two formats differ.

## -parameters

### -param pIMediaType [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type to compare.

### -param pdwFlags [out]

Receives a bitwise <b>OR</b> of zero or more flags, indicating the degree of similarity between the two media types. The following flags are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_MEDIATYPE_EQUAL_MAJOR_TYPES"></a><a id="mf_mediatype_equal_major_types"></a><dl>
<dt><b>MF_MEDIATYPE_EQUAL_MAJOR_TYPES</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The major types are the same. The major type is specified by the <a href="/windows/desktop/medfound/mf-mt-major-type-attribute">MF_MT_MAJOR_TYPE</a> attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_MEDIATYPE_EQUAL_FORMAT_TYPES"></a><a id="mf_mediatype_equal_format_types"></a><dl>
<dt><b>MF_MEDIATYPE_EQUAL_FORMAT_TYPES</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
The subtypes are the same, or neither media type has a subtype. The subtype is specified by the <a href="/windows/desktop/medfound/mf-mt-subtype-attribute">MF_MT_SUBTYPE</a> attribute.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_MEDIATYPE_EQUAL_FORMAT_DATA"></a><a id="mf_mediatype_equal_format_data"></a><dl>
<dt><b>MF_MEDIATYPE_EQUAL_FORMAT_DATA</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The attributes in one of the media types are a  subset of the attributes in the other, and the values of these attributes match, excluding the value of the <a href="/windows/desktop/medfound/mf-mt-user-data-attribute">MF_MT_USER_DATA</a>, <a href="/windows/desktop/medfound/mf-mt-frame-rate-range-min">MF_MT_FRAME_RATE_RANGE_MIN</a>,  and <a href="/windows/desktop/medfound/mf-mt-frame-rate-range-max">MF_MT_FRAME_RATE_RANGE_MAX</a> attributes.

Specifically, the method takes the media type with the smaller number of attributes and checks whether each attribute from that type is present in the other media type and has the same value (not including <a href="/windows/desktop/medfound/mf-mt-user-data-attribute">MF_MT_USER_DATA</a>, <a href="/windows/desktop/medfound/mf-mt-frame-rate-range-min">MF_MT_FRAME_RATE_RANGE_MIN</a>,  and <a href="/windows/desktop/medfound/mf-mt-frame-rate-range-max">MF_MT_FRAME_RATE_RANGE_MAX</a>). 

To perform other comparisons, use the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-compare">IMFAttributes::Compare</a> method. For example, the <b>Compare</b> method can test for identical attributes, or test the intersection of the two attribute sets. For more information, see <a href="/windows/desktop/api/mfobjects/ne-mfobjects-mf_attributes_match_type">MF_ATTRIBUTES_MATCH_TYPE</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_MEDIATYPE_EQUAL_FORMAT_USER_DATA"></a><a id="mf_mediatype_equal_format_user_data"></a><dl>
<dt><b>MF_MEDIATYPE_EQUAL_FORMAT_USER_DATA</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
The user data is identical, or neither media type contains user data. User data is specified by the <a href="/windows/desktop/medfound/mf-mt-user-data-attribute">MF_MT_USER_DATA</a> attribute.

</td>
</tr>
</table>

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The types are not equal. Examine the <i>pdwFlags</i> parameter to determine how the types differ.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The types are equal.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or both media types are invalid.
              

</td>
</tr>
</table>

## -remarks

Both of the media types must have a major type, or the method returns <b>E_INVALIDARG</b>.
      

If the method succeeds and all of the comparison flags are set in <i>pdwFlags</i>, the return value is <b>S_OK</b>. If the method succeeds but one or more comparison flags are not set, the method returns <b>S_FALSE</b>.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-compare">IMFAttributes::Compare</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a>