---
UID: NF:wmsdkidl.IWMWriterNetworkSink.Open
title: IWMWriterNetworkSink::Open
author: windows-sdk-content
description: The Open method opens a network port, and starts listening for network connections.
old-location: wmformat\iwmwriternetworksink_open.htm
tech.root: wmformat
ms.assetid: 2cfd4693-794c-46c8-b72d-b7529c63f16e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMWriterNetworkSink interface [windows Media Format],Open method, IWMWriterNetworkSink.Open, IWMWriterNetworkSink::Open, IWMWriterNetworkSinkOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMWriterNetworkSink interface, wmformat.iwmwriternetworksink_open, wmsdkidl/IWMWriterNetworkSink::Open
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
 - IWMWriterNetworkSink.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterNetworkSink::Open


## -description



The <b>Open</b> method opens a network port, and starts listening for network connections.




## -parameters




### -param pdwPortNum [in, out]

On input, pointer to a variable that specifies the port number. Set this value to zero if you want the network sink to select a suitable port. On output, the variable receives the port number that was used.


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
The <i>pdwPortNum</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The network sink is already open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_NETWORK_RESOURCE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The port number specified is already in use.

</td>
</tr>
</table>
 




## -remarks



This method binds the port. To release the port, call <a href="https://msdn.microsoft.com/en-us/library/Dd798762(v=VS.85).aspx">IWMWriterNetworkSink::Close</a>.

See the Remarks and Example Code sections for <a href="https://msdn.microsoft.com/en-us/library/Dd757474(v=VS.85).aspx">IWMWriter::BeginWriting</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798761(v=VS.85).aspx">IWMWriterNetworkSink Interface</a>
 

 

