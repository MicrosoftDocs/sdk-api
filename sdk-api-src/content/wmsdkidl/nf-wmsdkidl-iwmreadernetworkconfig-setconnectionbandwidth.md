---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetConnectionBandwidth
title: IWMReaderNetworkConfig::SetConnectionBandwidth
author: windows-sdk-content
description: The SetConnectionBandwidth method specifies the connection bandwidth for the client.
old-location: wmformat\iwmreadernetworkconfig_setconnectionbandwidth.htm
old-project: wmformat
ms.assetid: beb84e1b-ebe2-40a0-bcf0-eded9346d7a1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetConnectionBandwidth method, IWMReaderNetworkConfig.SetConnectionBandwidth, IWMReaderNetworkConfig::SetConnectionBandwidth, IWMReaderNetworkConfigSetConnectionBandwidth, SetConnectionBandwidth, SetConnectionBandwidth method [windows Media Format], SetConnectionBandwidth method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setconnectionbandwidth, wmsdkidl/IWMReaderNetworkConfig::SetConnectionBandwidth
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
-	IWMReaderNetworkConfig.SetConnectionBandwidth
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderNetworkConfig::SetConnectionBandwidth


## -description



The <b>SetConnectionBandwidth</b> method specifies the connection bandwidth for the client.




## -parameters




### -param dwConnectionBandwidth [in]

Specifies the maximum bandwidth for the connection, in bits per second. Specify zero for the reader to automatically detect the bandwidth


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



By default, the SDK automatically detects the bandwidth of the connection to the server. When auto-detection is set, a call to <b>GetConnectionBandwidth</b> following the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> request returns the dynamically detected connection bandwidth.

Setting a bandwidth by using this method is sometimes called <i>bandwidth-throttling</i> because it deliberately limits the available bandwidth.




## -see-also




<a href="https://msdn.microsoft.com/0957ece7-93fe-411b-b69e-fd03933b09d1">IWMReaderNetworkConfig Interface</a>



<a href="https://msdn.microsoft.com/cbbc945d-91ea-4d21-a1ac-2fcbcb081447">IWMReaderNetworkConfig::GetConnectionBandwidth</a>
 

 

