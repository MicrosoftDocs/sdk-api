---
UID: NF:wmsdkidl.IWMSyncReader2.SetRangeByFrameEx
title: IWMSyncReader2::SetRangeByFrameEx
author: windows-sdk-content
description: The SetRangeByFrameEx method configures the synchronous reader to read a portion of the file specified by a starting video frame number and a number of frames to read. This method also retrieves the presentation time of the requested frame number.
old-location: wmformat\iwmsyncreader2_setrangebyframeex.htm
tech.root: wmformat
ms.assetid: 8a21529f-3645-4fe5-900e-19032d601ff4
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWMSyncReader2 interface [windows Media Format],SetRangeByFrameEx method, IWMSyncReader2.SetRangeByFrameEx, IWMSyncReader2::SetRangeByFrameEx, IWMSyncReader2SetRangeByFrameEx, SetRangeByFrameEx, SetRangeByFrameEx method [windows Media Format], SetRangeByFrameEx method [windows Media Format],IWMSyncReader2 interface, wmformat.iwmsyncreader2_setrangebyframeex, wmsdkidl/IWMSyncReader2::SetRangeByFrameEx
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
 - IWMSyncReader2.SetRangeByFrameEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMSyncReader2::SetRangeByFrameEx


## -description



The <b>SetRangeByFrameEx</b> method configures the synchronous reader to read a portion of the file specified by a starting video frame number and a number of frames to read. This method also retrieves the presentation time of the requested frame number.




## -parameters




### -param wStreamNum [in]

Stream number.


### -param qwFrameNumber [in]

Frame number at which to begin playback. The first frame in a file is number 1.


### -param cFramesToRead [in]

Count of frames to read. Pass 0 to continue playback to the end of the file.


### -param pcnsStartTime [out]

Start time in 100-nanosecond units.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



By getting the presentation time of the requested frame number, you can avoid problems caused by seeking to a delta frame. The synchronous reader begins delivering samples at key frame boundaries. You can ignore frames until you reach the presentation time of your target frame.

The file must be frame-indexed. If the call is successful, all streams are synchronized to the same position based on time.




## -see-also




<a href="https://msdn.microsoft.com/f3db7530-a662-46f1-bc64-1dd4523dc87c">IWMSyncReader2 Interface</a>



<a href="https://msdn.microsoft.com/3d53838c-0d07-4aa6-8797-9ed7e07cb8fe">IWMSyncReader::SetRangeByFrame</a>
 

 

