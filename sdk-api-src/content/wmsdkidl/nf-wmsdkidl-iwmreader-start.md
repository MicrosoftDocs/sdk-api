---
UID: NF:wmsdkidl.IWMReader.Start
title: IWMReader::Start (wmsdkidl.h)
description: The Start method causes the reader object to start reading from the specified starting time offset. As data is read, it is passed to the application through the application's IWMReaderCallback::OnSample callback method.helpviewer_keywords: ["IWMReader interface [windows Media Format]","Start method","IWMReader.Start","IWMReader::Start","IWMReaderStart","Start","Start method [windows Media Format]","Start method [windows Media Format]","IWMReader interface","wmformat.iwmreader_start","wmsdkidl/IWMReader::Start"]
old-location: wmformat\iwmreader_start.htm
tech.root: wmformat
ms.assetid: 485844c6-7a84-4a0d-827d-060d8caef6cc
ms.date: 12/05/2018
ms.keywords: IWMReader interface [windows Media Format],Start method, IWMReader.Start, IWMReader::Start, IWMReaderStart, Start, Start method [windows Media Format], Start method [windows Media Format],IWMReader interface, wmformat.iwmreader_start, wmsdkidl/IWMReader::Start
f1_keywords:
- wmsdkidl/IWMReader.Start
dev_langs:
- c++
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
- IWMReader.Start
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReader::Start


## -description



The <b>Start</b> method causes the reader object to start reading from the specified starting time offset. As data is read, it is passed to the application through the application's <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample">IWMReaderCallback::OnSample</a> callback method.




## -parameters




### -param cnsStart [in]

Time within the file at which to start reading, in 100-nanosecond units. If <i>cnsStart</i> is set to WM_START_CURRENTPOSITION, playback starts from the current position.


### -param cnsDuration [in]

Duration of the read in 100-nanosecond units, or zero to read to the end of the file.


### -param fRate [in]

Playback speed. Normal speed is 1.0. Higher numbers cause faster playback, and numbers less than zero indicate reverse rate (rewinding). The valid ranges are 1.0 through 10.0, and -1.0 through -10.0.


### -param pvContext [in]

Generic pointer, for use by the application. This pointer is passed back to the <b>OnSample</b> method.


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
The value for <i>fRate</i> is not within the valid ranges, or the file is not seekable and a non-zero start position has been specified.

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



This method sends a WMT_STARTED status notification to the application's <b>IWMReaderCallback::OnStatus</b> function.

To change the rate but not the current file position, use the <b>Start</b> method with the WM_START_CURRENTPOSITION value.

Any call to <b>Start</b> while paused is treated as a <i>seek</i> through the file, and incurs a buffering penalty from network files. This is true even for calls to <b>Start</b> with the WM_START_CURRENTPOSITION value. To continue playing from the current paused position with no buffering penalty, call <b>Resume</b>.

If the application is providing the clock (by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock">IWMReaderAdvanced::SetUserProvidedClock</a>), it should usually set the <i>cnsDuration</i> parameter to zero. If the application specifies a non-zero value, then it must call the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime">IWMReaderAdvanced::DeliverTime</a> method exactly once, and the value passed to <b>DeliverTime</b> must be either the stop time or <code>(QWORD)-1</code>. The reader object will then deliver samples up to the specified duration.

This method is very similar to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker">IWMReaderAdvanced2::StartAtMarker</a> method, but that method uses a <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">marker</a> instead of a start time.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-stop">IWMReader::Stop</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback Interface</a>
 

 

