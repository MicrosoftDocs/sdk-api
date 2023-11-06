---
UID: NF:wmsdkidl.IWMSyncReader.SetRange
title: IWMSyncReader::SetRange (wmsdkidl.h)
description: The SetRange method enables you to specify a start time and duration for playback by the synchronous reader.
helpviewer_keywords: ["IWMSyncReader interface [windows Media Format]","SetRange method","IWMSyncReader.SetRange","IWMSyncReader::SetRange","IWMSyncReaderSetRange","SetRange","SetRange method [windows Media Format]","SetRange method [windows Media Format]","IWMSyncReader interface","wmformat.iwmsyncreader_setrange","wmsdkidl/IWMSyncReader::SetRange"]
old-location: wmformat\iwmsyncreader_setrange.htm
tech.root: wmformat
ms.assetid: d96c97ad-085d-4753-8efb-8a6bcb284e78
ms.date: 4/26/2023
ms.keywords: IWMSyncReader interface [windows Media Format],SetRange method, IWMSyncReader.SetRange, IWMSyncReader::SetRange, IWMSyncReaderSetRange, SetRange, SetRange method [windows Media Format], SetRange method [windows Media Format],IWMSyncReader interface, wmformat.iwmsyncreader_setrange, wmsdkidl/IWMSyncReader::SetRange
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMSyncReader::SetRange
 - wmsdkidl/IWMSyncReader::SetRange
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
 - IWMSyncReader.SetRange
---

# IWMSyncReader::SetRange


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetRange</b> method enables you to specify a start time and duration for playback by the synchronous reader.

## -parameters

### -param cnsStartTime [in]

Offset into the file at which to start playback. This value is measured in 100-nanosecond units.

### -param cnsDuration [in]

Duration in 100-nanosecond units, or zero to continue playback to the end of the file.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>cnsDuration</i> parameter is negative.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate memory for an internal object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
No file is loaded in the synchronous reader.

</td>
</tr>
</table>

## -remarks

This method specifies a range for the whole file only. You cannot specify a range for an individual stream.

You can call <b>SetRange</b> at any time after a file has been loaded.

The start time you specify might not be the presentation time of the first sample received. The synchronous delivers video samples starting with the key frame before the specified time.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe">IWMSyncReader::SetRangeByFrame</a>