---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetConnectionBandwidth
title: IWMReaderNetworkConfig::SetConnectionBandwidth (wmsdkidl.h)
description: The SetConnectionBandwidth method specifies the connection bandwidth for the client.helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","SetConnectionBandwidth method","IWMReaderNetworkConfig.SetConnectionBandwidth","IWMReaderNetworkConfig::SetConnectionBandwidth","IWMReaderNetworkConfigSetConnectionBandwidth","SetConnectionBandwidth","SetConnectionBandwidth method [windows Media Format]","SetConnectionBandwidth method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_setconnectionbandwidth","wmsdkidl/IWMReaderNetworkConfig::SetConnectionBandwidth"]
old-location: wmformat\iwmreadernetworkconfig_setconnectionbandwidth.htm
tech.root: wmformat
ms.assetid: beb84e1b-ebe2-40a0-bcf0-eded9346d7a1
ms.date: 12/05/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetConnectionBandwidth method, IWMReaderNetworkConfig.SetConnectionBandwidth, IWMReaderNetworkConfig::SetConnectionBandwidth, IWMReaderNetworkConfigSetConnectionBandwidth, SetConnectionBandwidth, SetConnectionBandwidth method [windows Media Format], SetConnectionBandwidth method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setconnectionbandwidth, wmsdkidl/IWMReaderNetworkConfig::SetConnectionBandwidth
f1_keywords:
- wmsdkidl/IWMReaderNetworkConfig.SetConnectionBandwidth
dev_langs:
- c++
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
- IWMReaderNetworkConfig.SetConnectionBandwidth
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



By default, the SDK automatically detects the bandwidth of the connection to the server. When auto-detection is set, a call to <b>GetConnectionBandwidth</b> following the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-open">Open</a> request returns the dynamically detected connection bandwidth.

Setting a bandwidth by using this method is sometimes called <i>bandwidth-throttling</i> because it deliberately limits the available bandwidth.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getconnectionbandwidth">IWMReaderNetworkConfig::GetConnectionBandwidth</a>
 

 

