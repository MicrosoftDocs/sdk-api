---
UID: NF:wmsdkidl.IWMSyncReader.SetRangeByFrame
title: IWMSyncReader::SetRangeByFrame
author: windows-sdk-content
description: The SetRangeByFrame method configures the synchronous reader to read a portion of the file specified by a starting video frame number and a number of frames to read.
old-location: wmformat\iwmsyncreader_setrangebyframe.htm
tech.root: wmformat
ms.assetid: 3d53838c-0d07-4aa6-8797-9ed7e07cb8fe
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMSyncReader interface [windows Media Format],SetRangeByFrame method, IWMSyncReader.SetRangeByFrame, IWMSyncReader::SetRangeByFrame, IWMSyncReaderSetRangeByFrame, SetRangeByFrame, SetRangeByFrame method [windows Media Format], SetRangeByFrame method [windows Media Format],IWMSyncReader interface, wmformat.iwmsyncreader_setrangebyframe, wmsdkidl/IWMSyncReader::SetRangeByFrame
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSyncReader::SetRangeByFrame


## -description



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



If the call is successful, all streams are synchronized to the same position based on the presentation time of the selected frame. Subsequent calls to <a href="https://msdn.microsoft.com/948047b3-3b87-4381-9320-c9602716ade2">GetNextSample</a> will retrieve samples for all active streams, not just the stream specified in the call to <b>SetRangeByFrame</b>. If you want to receive only samples for a single video stream by frame, you must call <a href="https://msdn.microsoft.com/d62a61cb-3b5a-4ce8-9677-92e280449d26">SetStreamsSelected</a> and pass the desired stream number prior to calling <b>GetNextSample</b>.

To use <b>SetRangeByFrame</b>, the file in the synchronous reader must be indexed by frame numbers. You can configure the indexer object to index by frame numbers with a call to <a href="https://msdn.microsoft.com/b4ab9ad8-5fc7-43ce-ba2f-f32135a44a86">IWMIndexer2::Configure</a>. Then make a call to <a href="https://msdn.microsoft.com/67dfb0df-4883-49e1-a085-0b78db3967d0">IWMIndexer::StartIndexing</a> to index the file with the new settings.

When you set a range for compressed sample delivery using a starting frame number, the synchronous reader will deliver samples starting at the first key frame before the specified frame. If you want to identify the presentation time of a frame, use <a href="https://msdn.microsoft.com/8a21529f-3645-4fe5-900e-19032d601ff4">IWMSyncReader2::SetRangeByFrameEx</a>.

Passing a negative number results in an error.

You can call <b>SetRangeByFrame</b> at any time after a file has been loaded in the synchronous reader.




## -see-also




<a href="https://msdn.microsoft.com/00627b0c-4484-417a-8680-0fd97aac41fe">IWMIndexer Interface</a>



<a href="https://msdn.microsoft.com/2a46e79f-084e-4173-ad0f-211d3065d81a">IWMSyncReader Interface</a>



<a href="https://msdn.microsoft.com/8a21529f-3645-4fe5-900e-19032d601ff4">IWMSyncReader2::SetRangeByFrameEx</a>



<a href="https://msdn.microsoft.com/d96c97ad-085d-4753-8efb-8a6bcb284e78">IWMSyncReader::SetRange</a>
 

 

