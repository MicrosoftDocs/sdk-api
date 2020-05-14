---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetAcceleratedStreamingDuration
title: IWMReaderNetworkConfig2::GetAcceleratedStreamingDuration (wmsdkidl.h)
description: The GetAcceleratedStreamingDuration method retrieves the current accelerated streaming duration.helpviewer_keywords: ["GetAcceleratedStreamingDuration","GetAcceleratedStreamingDuration method [windows Media Format]","GetAcceleratedStreamingDuration method [windows Media Format]","IWMReaderNetworkConfig2 interface","IWMReaderNetworkConfig2 interface [windows Media Format]","GetAcceleratedStreamingDuration method","IWMReaderNetworkConfig2.GetAcceleratedStreamingDuration","IWMReaderNetworkConfig2::GetAcceleratedStreamingDuration","IWMReaderNetworkConfig2GetAcceleratedStreamingDuration","wmformat.iwmreadernetworkconfig2_getacceleratedstreamingduration","wmsdkidl/IWMReaderNetworkConfig2::GetAcceleratedStreamingDuration"]
old-location: wmformat\iwmreadernetworkconfig2_getacceleratedstreamingduration.htm
tech.root: wmformat
ms.assetid: a8feda02-113a-4763-b695-c4cd48781ade
ms.date: 12/05/2018
ms.keywords: GetAcceleratedStreamingDuration, GetAcceleratedStreamingDuration method [windows Media Format], GetAcceleratedStreamingDuration method [windows Media Format],IWMReaderNetworkConfig2 interface, IWMReaderNetworkConfig2 interface [windows Media Format],GetAcceleratedStreamingDuration method, IWMReaderNetworkConfig2.GetAcceleratedStreamingDuration, IWMReaderNetworkConfig2::GetAcceleratedStreamingDuration, IWMReaderNetworkConfig2GetAcceleratedStreamingDuration, wmformat.iwmreadernetworkconfig2_getacceleratedstreamingduration, wmsdkidl/IWMReaderNetworkConfig2::GetAcceleratedStreamingDuration
f1_keywords:
- wmsdkidl/IWMReaderNetworkConfig2.GetAcceleratedStreamingDuration
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2">IWMReaderNetworkConfig2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setacceleratedstreamingduration">IWMReaderNetworkConfig2::SetAcceleratedStreamingDuration</a>
 

 

