---
UID: NF:wmsdkidl.IWMHeaderInfo.AddMarker
title: IWMHeaderInfo::AddMarker (wmsdkidl.h)
description: The AddMarker method adds a marker, consisting of a name and a specific time, to the header section of the ASF file.
helpviewer_keywords: ["AddMarker","AddMarker method [windows Media Format]","AddMarker method [windows Media Format]","IWMHeaderInfo interface","AddMarker method [windows Media Format]","IWMHeaderInfo2 interface","AddMarker method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo interface [windows Media Format]","AddMarker method","IWMHeaderInfo.AddMarker","IWMHeaderInfo2 interface [windows Media Format]","AddMarker method","IWMHeaderInfo2::AddMarker","IWMHeaderInfo3 interface [windows Media Format]","AddMarker method","IWMHeaderInfo3::AddMarker","IWMHeaderInfo::AddMarker","IWMHeaderInfoAddMarker","wmformat.iwmheaderinfo_addmarker","wmsdkidl/IWMHeaderInfo2::AddMarker","wmsdkidl/IWMHeaderInfo3::AddMarker","wmsdkidl/IWMHeaderInfo::AddMarker"]
old-location: wmformat\iwmheaderinfo_addmarker.htm
tech.root: wmformat
ms.assetid: cfa111bb-7bbb-448a-b2db-d36637c01a52
ms.date: 4/26/2023
ms.keywords: AddMarker, AddMarker method [windows Media Format], AddMarker method [windows Media Format],IWMHeaderInfo interface, AddMarker method [windows Media Format],IWMHeaderInfo2 interface, AddMarker method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],AddMarker method, IWMHeaderInfo.AddMarker, IWMHeaderInfo2 interface [windows Media Format],AddMarker method, IWMHeaderInfo2::AddMarker, IWMHeaderInfo3 interface [windows Media Format],AddMarker method, IWMHeaderInfo3::AddMarker, IWMHeaderInfo::AddMarker, IWMHeaderInfoAddMarker, wmformat.iwmheaderinfo_addmarker, wmsdkidl/IWMHeaderInfo2::AddMarker, wmsdkidl/IWMHeaderInfo3::AddMarker, wmsdkidl/IWMHeaderInfo::AddMarker
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
 - IWMHeaderInfo::AddMarker
 - wmsdkidl/IWMHeaderInfo::AddMarker
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
 - IWMHeaderInfo.AddMarker
 - IWMHeaderInfo2.AddMarker
 - IWMHeaderInfo3.AddMarker
---

# IWMHeaderInfo::AddMarker


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddMarker</b> method adds a <a href="/windows/desktop/wmformat/wmformat-glossary">marker</a>, consisting of a name and a specific time, to the header section of the ASF file.

## -parameters

### -param pwszMarkerName [in]

Pointer to a wide-character null-terminated string containing the marker name. Marker names are limited to 5120 wide characters.

### -param cnsMarkerTime [in]

The marker time in 100-nanosecond increments.

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
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object cannot currently be configured.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pwszMarkerName</i> is not a valid pointer.

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

The writer does not support markers. When accessing <b>IWMheaderInfo</b> from the writer, calls to <b>AddMarker</b> will return E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker">IWMHeaderInfo::GetMarker</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker">IWMHeaderInfo::RemoveMarker</a>



<a href="/windows/desktop/wmformat/markers">Markers</a>