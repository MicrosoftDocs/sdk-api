---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetConnectionBandwidth
title: IWMReaderNetworkConfig::GetConnectionBandwidth
author: windows-sdk-content
description: The GetConnectionBandwidth method retrieves the connection bandwidth for the client.
old-location: wmformat\iwmreadernetworkconfig_getconnectionbandwidth.htm
old-project: wmformat
ms.assetid: cbbc945d-91ea-4d21-a1ac-2fcbcb081447
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetConnectionBandwidth, GetConnectionBandwidth method [windows Media Format], GetConnectionBandwidth method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetConnectionBandwidth method, IWMReaderNetworkConfig.GetConnectionBandwidth, IWMReaderNetworkConfig::GetConnectionBandwidth, IWMReaderNetworkConfigGetConnectionBandwidth, wmformat.iwmreadernetworkconfig_getconnectionbandwidth, wmsdkidl/IWMReaderNetworkConfig::GetConnectionBandwidth
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
 - IWMReaderNetworkConfig.GetConnectionBandwidth
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::GetConnectionBandwidth


## -description



The <b>GetConnectionBandwidth</b> method retrieves the connection bandwidth for the client.




## -parameters




### -param pdwConnectionBandwidth [out]

Pointer to a <b>DWORD</b> containing the connection bandwidth, in bits per second.


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
NULL or invalid argument passed in.

</td>
</tr>
</table>
 




## -remarks



If this method returns zero, the bandwidth could not be detected. If the application has not called <b>SetConnectionBandwidth</b> (or called it with a zero parameter), the return value is the connection rate detected by the reader.

If you want to determine the connection bandwidth before receiving a sample, use this method.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/beb84e1b-ebe2-40a0-bcf0-eded9346d7a1">IWMReaderNetworkConfig::SetConnectionBandwidth</a>
 

 

