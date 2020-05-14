---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetEnableHTTP
title: IWMReaderNetworkConfig::SetEnableHTTP (wmsdkidl.h)
description: The SetEnableHTTP method enables or disables HTTP.helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","SetEnableHTTP method","IWMReaderNetworkConfig.SetEnableHTTP","IWMReaderNetworkConfig::SetEnableHTTP","IWMReaderNetworkConfigSetEnableHTTP","SetEnableHTTP","SetEnableHTTP method [windows Media Format]","SetEnableHTTP method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_setenablehttp","wmsdkidl/IWMReaderNetworkConfig::SetEnableHTTP"]
old-location: wmformat\iwmreadernetworkconfig_setenablehttp.htm
tech.root: wmformat
ms.assetid: 20667a28-e6e0-4ec0-905b-6735291063db
ms.date: 12/05/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetEnableHTTP method, IWMReaderNetworkConfig.SetEnableHTTP, IWMReaderNetworkConfig::SetEnableHTTP, IWMReaderNetworkConfigSetEnableHTTP, SetEnableHTTP, SetEnableHTTP method [windows Media Format], SetEnableHTTP method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setenablehttp, wmsdkidl/IWMReaderNetworkConfig::SetEnableHTTP
f1_keywords:
- wmsdkidl/IWMReaderNetworkConfig.SetEnableHTTP
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
- IWMReaderNetworkConfig.SetEnableHTTP
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderNetworkConfig::SetEnableHTTP


## -description



The <b>SetEnableHTTP</b> method enables or disables HTTP.




## -parameters




### -param fEnableHTTP [in]

Boolean value that is True if HTTP is to be enabled. Set this value to true if the reader can use HTTP when selecting a protocol for streaming.


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



This setting applies only to a protocol rollover or MMS:// URL. Even if this setting is disabled, the application can still specify an explicit HTTP://URL and stream successfully.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getenablehttp">IWMReaderNetworkConfig::GetEnableHTTP</a>
 

 

