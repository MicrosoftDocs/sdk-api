---
UID: NF:wmsdkidl.IWMWriterNetworkSink.Disconnect
title: IWMWriterNetworkSink::Disconnect
author: windows-sdk-content
description: The Disconnect method disconnects all clients from the network sink.
old-location: wmformat\iwmwriternetworksink_disconnect.htm
tech.root: wmformat
ms.assetid: cf4f294c-148c-469f-83e7-c2cd1c585aa3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Disconnect, Disconnect method [windows Media Format], Disconnect method [windows Media Format],IWMWriterNetworkSink interface, IWMWriterNetworkSink interface [windows Media Format],Disconnect method, IWMWriterNetworkSink.Disconnect, IWMWriterNetworkSink::Disconnect, IWMWriterNetworkSinkDisconnect, wmformat.iwmwriternetworksink_disconnect, wmsdkidl/IWMWriterNetworkSink::Disconnect
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMWriterNetworkSink.Disconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterNetworkSink::Disconnect


## -description



The <b>Disconnect</b> method disconnects all clients from the network sink.




## -parameters






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
</table>
 




## -remarks



This method is equivalent to the <a href="https://msdn.microsoft.com/en-us/library/Dd798762(v=VS.85).aspx">IWMWriterNetworkSink::Close</a> method, except that it does not release the port.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd798761(v=VS.85).aspx">IWMWriterNetworkSink Interface</a>
 

 

