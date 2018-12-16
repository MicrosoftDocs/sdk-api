---
UID: NF:wmsdkidl.IWMReaderAdvanced2.StartAtMarker
title: IWMReaderAdvanced2::StartAtMarker
author: windows-sdk-content
description: The StartAtMarker method starts the reader from a specified marker.
old-location: wmformat\iwmreaderadvanced2_startatmarker.htm
tech.root: wmformat
ms.assetid: 444adb2f-4289-4950-8841-07353479ef43
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderAdvanced2 interface [windows Media Format],StartAtMarker method, IWMReaderAdvanced2.StartAtMarker, IWMReaderAdvanced2::StartAtMarker, IWMReaderAdvanced2StartAtMarker, StartAtMarker, StartAtMarker method [windows Media Format], StartAtMarker method [windows Media Format],IWMReaderAdvanced2 interface, wmformat.iwmreaderadvanced2_startatmarker, wmsdkidl/IWMReaderAdvanced2::StartAtMarker
ms.topic: method
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
 - IWMReaderAdvanced2.StartAtMarker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAdvanced2::StartAtMarker


## -description



The <b>StartAtMarker</b> method starts the reader from a specified <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">marker</a>.




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



This method is very similar to <a href="https://msdn.microsoft.com/en-us/library/Dd743608(v=VS.85).aspx">IWMReader::Start</a>. The difference is that this method uses a marker index but <b>IWMReader::Start</b> uses a start time.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757430(v=VS.85).aspx">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/ba9bc93e-76a9-4a49-951f-c38dbcceef8c">Markers</a>



<a href="https://msdn.microsoft.com/b801c985-4ec7-441e-9f8a-40c69b1299a9">Using Markers</a>
 

 

