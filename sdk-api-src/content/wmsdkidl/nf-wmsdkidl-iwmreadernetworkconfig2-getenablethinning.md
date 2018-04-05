---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetEnableThinning
title: IWMReaderNetworkConfig2::GetEnableThinning method
author: windows-driver-content
description: The GetEnableThinning method ascertains whether Intelligent Streaming is enabled. Intelligent Streaming is the communication between the reader and the streaming server that enables the server to change the content sent based on available bandwidth.
old-location: wmformat\iwmreadernetworkconfig2_getenablethinning.htm
old-project: wmformat
ms.assetid: 3ad43406-56db-48db-96a7-419b6719dbd4
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetEnableThinning method [windows Media Format], GetEnableThinning method [windows Media Format], IWMReaderNetworkConfig2 interface, GetEnableThinning,IWMReaderNetworkConfig2.GetEnableThinning, IWMReaderNetworkConfig2, IWMReaderNetworkConfig2 interface [windows Media Format], GetEnableThinning method, IWMReaderNetworkConfig2::GetEnableThinning, IWMReaderNetworkConfig2GetEnableThinning, wmformat.iwmreadernetworkconfig2_getenablethinning, wmsdkidl/IWMReaderNetworkConfig2::GetEnableThinning
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderNetworkConfig2.GetEnableThinning
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig2::GetEnableThinning method


## -description



The <b>GetEnableThinning</b> method ascertains whether Intelligent Streaming is enabled. Intelligent Streaming is the communication between the reader and the streaming server that enables the server to change the content sent based on available bandwidth.




## -parameters




### -param pfEnableThinning [out]

Pointer to a variable that receives a Boolean value. The value is <b>TRUE</b> if thinning is enabled, or <b>FALSE</b> if thinning is disabled.


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



With Intelligent Streaming enabled, the reader responds to insufficient bandwidth by requesting that the server reduce the bit rate by using one of the following techniques. If one technique does not solve the problem, the reader will try the next one:

<ul>
<li>If the file is encoded using multiple bit rates (MBR), the first step the reader takes to rectify insufficient bandwidth is to request a lower bit rate version of streams.</li>
<li>If the file is not MBR, or if using a lower bit rate stream does not reduce the bandwidth requirements enough, the reader requests that the server thin the video streams. This means that the server reduces the frame rate of the video being streamed.</li>
<li>If thinning the video streams does not reduce the bandwidth requirements enough, the reader requests that the server stop sending video streams.</li>
</ul>
If Intelligent Streaming is disabled by setting <i>pfEnableThinning</i> to <b>FALSE</b>, the reader will not request any bandwidth corrections.

This feature applies only to content streaming from a server running Windows Media Services.




## -see-also




<a href="https://msdn.microsoft.com/a0480243-53e0-4da5-a119-291b19f46951">IWMReaderNetworkConfig2 Interface</a>



<a href="https://msdn.microsoft.com/98d4eb7e-e712-4ca0-a532-1160254748b8">IWMReaderNetworkConfig2::SetEnableThinning</a>
 

 

