---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.SetAcceleratedStreamingDuration
title: IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration
author: windows-sdk-content
description: The SetAcceleratedStreamingDuration method sets the accelerated streaming duration. This duration applies to the Fast Start feature of Windows Media Services, which enables content to be played quickly without waiting for lengthy initial buffering.
old-location: wmformat\iwmreadernetworkconfig2_setacceleratedstreamingduration.htm
tech.root: wmformat
ms.assetid: c9ad5064-7742-4145-b560-f3e867da609a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMReaderNetworkConfig2 interface [windows Media Format],SetAcceleratedStreamingDuration method, IWMReaderNetworkConfig2.SetAcceleratedStreamingDuration, IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration, IWMReaderNetworkConfig2SetAcceleratedStreamingDuration, SetAcceleratedStreamingDuration, SetAcceleratedStreamingDuration method [windows Media Format], SetAcceleratedStreamingDuration method [windows Media Format],IWMReaderNetworkConfig2 interface, wmformat.iwmreadernetworkconfig2_setacceleratedstreamingduration, wmsdkidl/IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration
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
 - IWMReaderNetworkConfig2.SetAcceleratedStreamingDuration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration


## -description



The <b>SetAcceleratedStreamingDuration</b> method sets the accelerated streaming duration. This duration applies to the Fast Start feature of Windows Media Services, which enables content to be played quickly without waiting for lengthy initial buffering.




## -parameters




### -param cnsAccelDuration [in]

Specifies the accelerated streaming duration, in 100-nanosecond units. The maximum value is 1,200,000,000. This is the amount of data at the beginning of the content that is streamed at an accelerated rate.


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
</table>
 




## -remarks



When using Fast Start, the server running Windows Media Services will send some data at the beginning of the content at a faster rate than that specified by the bit rate of the content.




## -see-also




<a href="https://msdn.microsoft.com/a0480243-53e0-4da5-a119-291b19f46951">IWMReaderNetworkConfig2 Interface</a>



<a href="https://msdn.microsoft.com/a8feda02-113a-4763-b695-c4cd48781ade">IWMReaderNetworkConfig2::GetAcceleratedStreamingDuration</a>
 

 

