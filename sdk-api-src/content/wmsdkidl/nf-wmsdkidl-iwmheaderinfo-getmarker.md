---
UID: NF:wmsdkidl.IWMHeaderInfo.GetMarker
title: IWMHeaderInfo::GetMarker (wmsdkidl.h)
description: The GetMarker method returns the name and time of a marker.
helpviewer_keywords: ["GetMarker","GetMarker method [windows Media Format]","GetMarker method [windows Media Format]","IWMHeaderInfo interface","GetMarker method [windows Media Format]","IWMHeaderInfo2 interface","GetMarker method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo interface [windows Media Format]","GetMarker method","IWMHeaderInfo.GetMarker","IWMHeaderInfo2 interface [windows Media Format]","GetMarker method","IWMHeaderInfo2::GetMarker","IWMHeaderInfo3 interface [windows Media Format]","GetMarker method","IWMHeaderInfo3::GetMarker","IWMHeaderInfo::GetMarker","IWMHeaderInfoGetMarker","wmformat.iwmheaderinfo_getmarker","wmsdkidl/IWMHeaderInfo2::GetMarker","wmsdkidl/IWMHeaderInfo3::GetMarker","wmsdkidl/IWMHeaderInfo::GetMarker"]
old-location: wmformat\iwmheaderinfo_getmarker.htm
tech.root: wmformat
ms.assetid: ae035991-86c8-4ffc-b819-5a5ce81a980f
ms.date: 12/05/2018
ms.keywords: GetMarker, GetMarker method [windows Media Format], GetMarker method [windows Media Format],IWMHeaderInfo interface, GetMarker method [windows Media Format],IWMHeaderInfo2 interface, GetMarker method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],GetMarker method, IWMHeaderInfo.GetMarker, IWMHeaderInfo2 interface [windows Media Format],GetMarker method, IWMHeaderInfo2::GetMarker, IWMHeaderInfo3 interface [windows Media Format],GetMarker method, IWMHeaderInfo3::GetMarker, IWMHeaderInfo::GetMarker, IWMHeaderInfoGetMarker, wmformat.iwmheaderinfo_getmarker, wmsdkidl/IWMHeaderInfo2::GetMarker, wmsdkidl/IWMHeaderInfo3::GetMarker, wmsdkidl/IWMHeaderInfo::GetMarker
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMHeaderInfo::GetMarker
 - wmsdkidl/IWMHeaderInfo::GetMarker
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
 - qasf.dll
api_name:
 - IWMHeaderInfo.GetMarker
 - IWMHeaderInfo2.GetMarker
 - IWMHeaderInfo3.GetMarker
---

# IWMHeaderInfo::GetMarker


## -description

The <b>GetMarker</b> method returns the name and time of a <a href="/windows/desktop/wmformat/wmformat-glossary">marker</a>.

## -parameters

### -param wIndex [in]

<b>WORD</b> containing the index.

### -param pwszMarkerName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the marker name.

### -param pcchMarkerNameLen [in]

On input, a pointer to a variable containing the length of the <i>pwszMarkerName</i> array in wide characters (2 bytes). On output, if the method succeeds, the variable contains the actual length of the name, including the terminating <b>null</b> character. To retrieve the length of the name, you must set this to zero and set <i>pwszMarkerName</i> and <i>pcnsMarkerTime</i> to <b>NULL</b>.

### -param pcnsMarkerTime [out]

Pointer to a variable specifying the marker time in 100-nanosecond increments.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The size specified by <i>pcchMarkerNameLen</i> is too small to receive the name.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is not in a configurable state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pcchMarkerNameLen</i> is <b>NULL</b>, or another parameter does not contain a valid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>

## -remarks

The writer does not support markers, and returns E_NOTIMPL when this method is called.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker">IWMHeaderInfo::AddMarker</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount">IWMHeaderInfo::GetMarkerCount</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker">IWMHeaderInfo::RemoveMarker</a>



<a href="/windows/desktop/wmformat/markers">Markers</a>