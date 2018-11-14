---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetAcceleratedStreamingDuration
title: IWMReaderNetworkConfig2::GetAcceleratedStreamingDuration
author: windows-sdk-content
description: The GetAcceleratedStreamingDuration method retrieves the current accelerated streaming duration.
old-location: wmformat\iwmreadernetworkconfig2_getacceleratedstreamingduration.htm
tech.root: wmformat
ms.assetid: a8feda02-113a-4763-b695-c4cd48781ade
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetAcceleratedStreamingDuration, GetAcceleratedStreamingDuration method [windows Media Format], GetAcceleratedStreamingDuration method [windows Media Format],IWMReaderNetworkConfig2 interface, IWMReaderNetworkConfig2 interface [windows Media Format],GetAcceleratedStreamingDuration method, IWMReaderNetworkConfig2.GetAcceleratedStreamingDuration, IWMReaderNetworkConfig2::GetAcceleratedStreamingDuration, IWMReaderNetworkConfig2GetAcceleratedStreamingDuration, wmformat.iwmreadernetworkconfig2_getacceleratedstreamingduration, wmsdkidl/IWMReaderNetworkConfig2::GetAcceleratedStreamingDuration
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
 - IWMReaderNetworkConfig2.GetAcceleratedStreamingDuration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsdkidl.h
: 
- IWMReaderNetworkConfig2.GetAcceleratedStreamingDuration
: 
---

# IWMReaderNetworkConfig2::GetAcceleratedStreamingDuration


## -description



The <b>GetAcceleratedStreamingDuration</b> method retrieves the current accelerated streaming duration. This duration applies to the Fast Start feature of Windows Media Services, which enables content to be played quickly without waiting for lengthy initial buffering.




## -parameters




### -param pcnsAccelDuration [out]

Pointer to a <b>QWORD</b> that receives the accelerated streaming duration, in 100-nanosecond units. This is the amount of data at the beginning of the content that is streamed at an accelerated rate. The default value is twice the buffering duration.


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
NULL pointer argument.

</td>
</tr>
</table>
 




## -remarks



When using Fast Start, the server running Windows Media Services will send some data at the beginning of the content at a faster rate than that specified by the bit rate of the content.




## -see-also




<a href="https://msdn.microsoft.com/a0480243-53e0-4da5-a119-291b19f46951">IWMReaderNetworkConfig2 Interface</a>



<a href="https://msdn.microsoft.com/c9ad5064-7742-4145-b560-f3e867da609a">IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration</a>
 

 

