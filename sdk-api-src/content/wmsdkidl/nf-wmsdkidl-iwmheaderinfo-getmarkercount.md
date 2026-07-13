---
UID: NF:wmsdkidl.IWMHeaderInfo.GetMarkerCount
title: IWMHeaderInfo::GetMarkerCount (wmsdkidl.h)
description: The GetMarkerCount method returns the number of markers currently in the header section of the ASF file.
helpviewer_keywords: ["GetMarkerCount","GetMarkerCount method [windows Media Format]","GetMarkerCount method [windows Media Format]","IWMHeaderInfo interface","GetMarkerCount method [windows Media Format]","IWMHeaderInfo2 interface","GetMarkerCount method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo interface [windows Media Format]","GetMarkerCount method","IWMHeaderInfo.GetMarkerCount","IWMHeaderInfo2 interface [windows Media Format]","GetMarkerCount method","IWMHeaderInfo2::GetMarkerCount","IWMHeaderInfo3 interface [windows Media Format]","GetMarkerCount method","IWMHeaderInfo3::GetMarkerCount","IWMHeaderInfo::GetMarkerCount","IWMHeaderInfoGetMarkerCount","wmformat.iwmheaderinfo_getmarkercount","wmsdkidl/IWMHeaderInfo2::GetMarkerCount","wmsdkidl/IWMHeaderInfo3::GetMarkerCount","wmsdkidl/IWMHeaderInfo::GetMarkerCount"]
old-location: wmformat\iwmheaderinfo_getmarkercount.htm
tech.root: wmformat
ms.assetid: c0d8e61d-8703-407a-9610-9e9f29ab92a1
ms.date: 4/26/2023
ms.keywords: GetMarkerCount, GetMarkerCount method [windows Media Format], GetMarkerCount method [windows Media Format],IWMHeaderInfo interface, GetMarkerCount method [windows Media Format],IWMHeaderInfo2 interface, GetMarkerCount method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],GetMarkerCount method, IWMHeaderInfo.GetMarkerCount, IWMHeaderInfo2 interface [windows Media Format],GetMarkerCount method, IWMHeaderInfo2::GetMarkerCount, IWMHeaderInfo3 interface [windows Media Format],GetMarkerCount method, IWMHeaderInfo3::GetMarkerCount, IWMHeaderInfo::GetMarkerCount, IWMHeaderInfoGetMarkerCount, wmformat.iwmheaderinfo_getmarkercount, wmsdkidl/IWMHeaderInfo2::GetMarkerCount, wmsdkidl/IWMHeaderInfo3::GetMarkerCount, wmsdkidl/IWMHeaderInfo::GetMarkerCount
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
 - IWMHeaderInfo::GetMarkerCount
 - wmsdkidl/IWMHeaderInfo::GetMarkerCount
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
 - IWMHeaderInfo.GetMarkerCount
 - IWMHeaderInfo2.GetMarkerCount
 - IWMHeaderInfo3.GetMarkerCount
---

# IWMHeaderInfo::GetMarkerCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetMarkerCount</b> method returns the number of <a href="/windows/desktop/wmformat/wmformat-glossary">markers</a> currently in the header section of the ASF file.

## -parameters

### -param pcMarkers [out]

Pointer to a count of markers.

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
The object is not in a configurable state.

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

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker">IWMHeaderInfo::GetMarker</a>



<a href="/windows/desktop/wmformat/markers">Markers</a>