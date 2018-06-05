---
UID: NF:wmsdkidl.IWMWriterNetworkSink.Close
title: IWMWriterNetworkSink::Close
author: windows-sdk-content
description: The Close method disconnects all clients from the network sink, and releases the port.
old-location: wmformat\iwmwriternetworksink_close.htm
old-project: wmformat
ms.assetid: 7e36b94b-e6d3-46a0-8874-edd545e0e5b1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: Close, Close method [windows Media Format], Close method [windows Media Format],IWMWriterNetworkSink interface, IWMWriterNetworkSink interface [windows Media Format],Close method, IWMWriterNetworkSink.Close, IWMWriterNetworkSink::Close, IWMWriterNetworkSinkClose, wmformat.iwmwriternetworksink_close, wmsdkidl/IWMWriterNetworkSink::Close
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
-	IWMWriterNetworkSink.Close
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterNetworkSink::Close


## -description



The <b>Close</b> method disconnects all clients from the network sink, and releases the port.




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
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The network sink is not connected.

</td>
</tr>
</table>
 




## -remarks



See the Remarks and Example Code sections for <a href="https://msdn.microsoft.com/df511ff0-a87b-442a-85bd-c8d924ab2047">IWMWriter::BeginWriting</a>.




## -see-also




<a href="https://msdn.microsoft.com/3204c360-f407-4cf3-bb21-7e6094587fb0">IWMWriterNetworkSink Interface</a>



<a href="https://msdn.microsoft.com/2cfd4693-794c-46c8-b72d-b7529c63f16e">IWMWriterNetworkSink::Open</a>
 

 

