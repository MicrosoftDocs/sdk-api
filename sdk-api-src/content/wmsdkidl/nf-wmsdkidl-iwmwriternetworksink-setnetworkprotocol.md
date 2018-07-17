---
UID: NF:wmsdkidl.IWMWriterNetworkSink.SetNetworkProtocol
title: IWMWriterNetworkSink::SetNetworkProtocol
author: windows-sdk-content
description: The SetNetworkProtocol method sets the network protocol that the network sink uses. Currently, HTTP is the only protocol supported by the network sink.
old-location: wmformat\iwmwriternetworksink_setnetworkprotocol.htm
old-project: wmformat
ms.assetid: 8ad6b2a4-b50b-45a0-8aa0-cabfc1e59bb7
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWMWriterNetworkSink interface [windows Media Format],SetNetworkProtocol method, IWMWriterNetworkSink.SetNetworkProtocol, IWMWriterNetworkSink::SetNetworkProtocol, IWMWriterNetworkSinkSetNetworkProtocol, SetNetworkProtocol, SetNetworkProtocol method [windows Media Format], SetNetworkProtocol method [windows Media Format],IWMWriterNetworkSink interface, wmformat.iwmwriternetworksink_setnetworkprotocol, wmsdkidl/IWMWriterNetworkSink::SetNetworkProtocol
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMWriterNetworkSink.SetNetworkProtocol
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterNetworkSink::SetNetworkProtocol


## -description



The <b>SetNetworkProtocol</b> method sets the network protocol that the network sink uses. Currently, HTTP is the only protocol supported by the network sink.




## -parameters




### -param protocol [in]

Specifies the procotcol, as a value from the <a href="https://msdn.microsoft.com/dc8b67a9-33fe-408b-b0b5-62a2b219b6b5">WMT_NET_PROTOCOL</a> enumeration type.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, the values shown in the following table.

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
Invalid argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3204c360-f407-4cf3-bb21-7e6094587fb0">IWMWriterNetworkSink Interface</a>



<a href="https://msdn.microsoft.com/5007b5be-9521-46f4-8e5c-85e70d48e99f">IWMWriterNetworkSink::GetNetworkProtocol</a>
 

 

