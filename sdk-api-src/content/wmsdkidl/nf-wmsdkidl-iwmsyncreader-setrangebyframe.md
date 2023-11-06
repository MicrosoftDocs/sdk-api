---
UID: NF:wmsdkidl.IWMSyncReader.SetRangeByFrame
title: IWMSyncReader::SetRangeByFrame (wmsdkidl.h)
description: The SetRangeByFrame method configures the synchronous reader to read a portion of the file specified by a starting video frame number and a number of frames to read.
helpviewer_keywords: ["IWMSyncReader interface [windows Media Format]","SetRangeByFrame method","IWMSyncReader.SetRangeByFrame","IWMSyncReader::SetRangeByFrame","IWMSyncReaderSetRangeByFrame","SetRangeByFrame","SetRangeByFrame method [windows Media Format]","SetRangeByFrame method [windows Media Format]","IWMSyncReader interface","wmformat.iwmsyncreader_setrangebyframe","wmsdkidl/IWMSyncReader::SetRangeByFrame"]
old-location: wmformat\iwmsyncreader_setrangebyframe.htm
tech.root: wmformat
ms.assetid: 3d53838c-0d07-4aa6-8797-9ed7e07cb8fe
ms.date: 4/26/2023
ms.keywords: IWMSyncReader interface [windows Media Format],SetRangeByFrame method, IWMSyncReader.SetRangeByFrame, IWMSyncReader::SetRangeByFrame, IWMSyncReaderSetRangeByFrame, SetRangeByFrame, SetRangeByFrame method [windows Media Format], SetRangeByFrame method [windows Media Format],IWMSyncReader interface, wmformat.iwmsyncreader_setrangebyframe, wmsdkidl/IWMSyncReader::SetRangeByFrame
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
 - IWMSyncReader::SetRangeByFrame
 - wmsdkidl/IWMSyncReader::SetRangeByFrame
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
 - IWMSyncReader.SetRangeByFrame
---

# IWMSyncReader::SetRangeByFrame


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetRangeByFrame</b> method configures the synchronous reader to read a portion of the file specified by a starting video frame number and a number of frames to read.

## -parameters

### -param wStreamNum [in]

Stream number.

### -param qwFrameNumber [in]

Frame number at which to begin playback. The first frame in a file is number 1.

### -param cFramesToRead [in]

Count of frames to read. Pass 0 to continue playback to the end of the file.

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
<i>cFramesToRead</i> contains a negative number.

</td>
</tr>
</table>

## -remarks

If the call is successful, all streams are synchronized to the same position based on the presentation time of the selected frame. Subsequent calls to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample">GetNextSample</a> will retrieve samples for all active streams, not just the stream specified in the call to <b>SetRangeByFrame</b>. If you want to receive only samples for a single video stream by frame, you must call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setstreamsselected">SetStreamsSelected</a> and pass the desired stream number prior to calling <b>GetNextSample</b>.

To use <b>SetRangeByFrame</b>, the file in the synchronous reader must be indexed by frame numbers. You can configure the indexer object to index by frame numbers with a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmindexer2-configure">IWMIndexer2::Configure</a>. Then make a call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing">IWMIndexer::StartIndexing</a> to index the file with the new settings.

When you set a range for compressed sample delivery using a starting frame number, the synchronous reader will deliver samples starting at the first key frame before the specified frame. If you want to identify the presentation time of a frame, use <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebyframeex">IWMSyncReader2::SetRangeByFrameEx</a>.

Passing a negative number results in an error.

You can call <b>SetRangeByFrame</b> at any time after a file has been loaded in the synchronous reader.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer">IWMIndexer Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setrangebyframeex">IWMSyncReader2::SetRangeByFrameEx</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange">IWMSyncReader::SetRange</a>