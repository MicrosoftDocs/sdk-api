---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.GetAutoReconnectLimit
title: IWMReaderNetworkConfig2::GetAutoReconnectLimit method
author: windows-driver-content
description: The GetAutoReconnectLimit method retrieves the maximum number of times the reader will attempt to reconnect to the server in the case of an unexpected disconnection.
old-location: wmformat\iwmreadernetworkconfig2_getautoreconnectlimit.htm
old-project: wmformat
ms.assetid: 8d0b794c-b3bf-4ec5-ac68-9666e73f7a6e
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetAutoReconnectLimit method [windows Media Format], GetAutoReconnectLimit method [windows Media Format], IWMReaderNetworkConfig2 interface, GetAutoReconnectLimit,IWMReaderNetworkConfig2.GetAutoReconnectLimit, IWMReaderNetworkConfig2, IWMReaderNetworkConfig2 interface [windows Media Format], GetAutoReconnectLimit method, IWMReaderNetworkConfig2::GetAutoReconnectLimit, IWMReaderNetworkConfig2GetAutoReconnectLimit, wmformat.iwmreadernetworkconfig2_getautoreconnectlimit, wmsdkidl/IWMReaderNetworkConfig2::GetAutoReconnectLimit
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
-	IWMReaderNetworkConfig2.GetAutoReconnectLimit
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig2::GetAutoReconnectLimit method


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




<a href="https://msdn.microsoft.com/a0480243-53e0-4da5-a119-291b19f46951">IWMReaderNetworkConfig2 Interface</a>



<a href="https://msdn.microsoft.com/0ef6bb5c-6369-4b80-a227-da790b1ab6da">IWMReaderNetworkConfig2::SetAutoReconnectLimit</a>
 

 

