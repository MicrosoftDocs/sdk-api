---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetMaxNetPacketSize
title: IWMReaderNetworkConfig2::GetMaxNetPacketSize
author: windows-sdk-content
description: The GetMaxNetPacketSize method retrieves the maximum size of packets being streamed over a network.
old-location: wmformat\iwmreadernetworkconfig2_getmaxnetpacketsize.htm
tech.root: wmformat
ms.assetid: 0249822c-4772-4317-aec2-e466fbd70bad
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetMaxNetPacketSize, GetMaxNetPacketSize method [windows Media Format], GetMaxNetPacketSize method [windows Media Format],IWMReaderNetworkConfig2 interface, IWMReaderNetworkConfig2 interface [windows Media Format],GetMaxNetPacketSize method, IWMReaderNetworkConfig2.GetMaxNetPacketSize, IWMReaderNetworkConfig2::GetMaxNetPacketSize, IWMReaderNetworkConfig2GetMaxNetPacketSize, wmformat.iwmreadernetworkconfig2_getmaxnetpacketsize, wmsdkidl/IWMReaderNetworkConfig2::GetMaxNetPacketSize
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
 - IWMReaderNetworkConfig2.GetMaxNetPacketSize
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
- IWMReaderNetworkConfig2.GetMaxNetPacketSize
: 
---

# IWMReaderNetworkConfig2::GetMaxNetPacketSize


## -description



The <b>GetMaxNetPacketSize</b> method retrieves the maximum size of packets being streamed over a network.




## -parameters




### -param pdwMaxNetPacketSize [out]

Pointer to a <b>DWORD</b> containing the maximum net packet size, in bytes.


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
 




## -see-also




<a href="https://msdn.microsoft.com/a0480243-53e0-4da5-a119-291b19f46951">IWMReaderNetworkConfig2 Interface</a>
 

 

