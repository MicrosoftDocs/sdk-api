---
UID: NF:wmsdkidl.IWMReaderAdvanced2.StartAtMarker
title: IWMReaderAdvanced2::StartAtMarker (wmsdkidl.h)
description: The StartAtMarker method starts the reader from a specified marker.
helpviewer_keywords: ["IWMReaderAdvanced2 interface [windows Media Format]","StartAtMarker method","IWMReaderAdvanced2.StartAtMarker","IWMReaderAdvanced2::StartAtMarker","IWMReaderAdvanced2StartAtMarker","StartAtMarker","StartAtMarker method [windows Media Format]","StartAtMarker method [windows Media Format]","IWMReaderAdvanced2 interface","wmformat.iwmreaderadvanced2_startatmarker","wmsdkidl/IWMReaderAdvanced2::StartAtMarker"]
old-location: wmformat\iwmreaderadvanced2_startatmarker.htm
tech.root: wmformat
ms.assetid: 444adb2f-4289-4950-8841-07353479ef43
ms.date: 4/26/2023
ms.keywords: IWMReaderAdvanced2 interface [windows Media Format],StartAtMarker method, IWMReaderAdvanced2.StartAtMarker, IWMReaderAdvanced2::StartAtMarker, IWMReaderAdvanced2StartAtMarker, StartAtMarker, StartAtMarker method [windows Media Format], StartAtMarker method [windows Media Format],IWMReaderAdvanced2 interface, wmformat.iwmreaderadvanced2_startatmarker, wmsdkidl/IWMReaderAdvanced2::StartAtMarker
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
 - IWMReaderAdvanced2::StartAtMarker
 - wmsdkidl/IWMReaderAdvanced2::StartAtMarker
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
api_name:
 - IWMReaderAdvanced2.StartAtMarker
---

# IWMReaderAdvanced2::StartAtMarker


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>StartAtMarker</b> method starts the reader from a specified <a href="/windows/desktop/wmformat/wmformat-glossary">marker</a>.

## -parameters

### -param wMarkerIndex [in]

<b>WORD</b> containing the marker index.

### -param cnsDuration [in]

Specifies the duration, in 100-nanosecond units.

### -param fRate [in]

Floating point number indicating rate. Normal-speed playback is 1.0; higher numbers cause faster playback. Numbers less than zero indicate reverse rate (rewinding). The valid range is 1.0 through 10.0, and -1.0 through -10.0.

### -param pvContext [in]

Generic pointer, for use by the application.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The value for <i>fRate</i> is not within the valid ranges.

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

This method is very similar to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">IWMReader::Start</a>. The difference is that this method uses a marker index but <b>IWMReader::Start</b> uses a start time.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="/windows/desktop/wmformat/markers">Markers</a>



<a href="/windows/desktop/wmformat/using-markers">Using Markers</a>