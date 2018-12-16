---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetAutoReconnectLimit
title: IWMReaderNetworkConfig2::GetAutoReconnectLimit
author: windows-sdk-content
description: The GetAutoReconnectLimit method retrieves the maximum number of times the reader will attempt to reconnect to the server in the case of an unexpected disconnection.
old-location: wmformat\iwmreadernetworkconfig2_getautoreconnectlimit.htm
tech.root: wmformat
ms.assetid: 8d0b794c-b3bf-4ec5-ac68-9666e73f7a6e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetAutoReconnectLimit, GetAutoReconnectLimit method [windows Media Format], GetAutoReconnectLimit method [windows Media Format],IWMReaderNetworkConfig2 interface, IWMReaderNetworkConfig2 interface [windows Media Format],GetAutoReconnectLimit method, IWMReaderNetworkConfig2.GetAutoReconnectLimit, IWMReaderNetworkConfig2::GetAutoReconnectLimit, IWMReaderNetworkConfig2GetAutoReconnectLimit, wmformat.iwmreadernetworkconfig2_getautoreconnectlimit, wmsdkidl/IWMReaderNetworkConfig2::GetAutoReconnectLimit
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
 - IWMReaderNetworkConfig2.GetAutoReconnectLimit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderNetworkConfig2::GetAutoReconnectLimit


## -description



The <b>GetAutoReconnectLimit</b> method retrieves the maximum number of times the reader will attempt to reconnect to the server in the case of an unexpected disconnection. This feature, called Fast Reconnect, applies only to content being streamed from a server running Windows Media Services.




## -parameters




### -param pdwAutoReconnectLimit [out]

Pointer to a <b>DWORD</b> containing the automatic reconnection limit.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd743505(v=VS.85).aspx">IWMReaderNetworkConfig2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743514(v=VS.85).aspx">IWMReaderNetworkConfig2::SetAutoReconnectLimit</a>
 

 

