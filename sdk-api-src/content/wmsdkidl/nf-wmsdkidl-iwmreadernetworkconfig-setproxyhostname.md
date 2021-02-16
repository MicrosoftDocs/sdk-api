---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetProxyHostName
title: IWMReaderNetworkConfig::SetProxyHostName (wmsdkidl.h)
description: The SetProxyHostName method specifies the proxy host name.
helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","SetProxyHostName method","IWMReaderNetworkConfig.SetProxyHostName","IWMReaderNetworkConfig::SetProxyHostName","IWMReaderNetworkConfigSetProxyHostName","SetProxyHostName","SetProxyHostName method [windows Media Format]","SetProxyHostName method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_setproxyhostname","wmsdkidl/IWMReaderNetworkConfig::SetProxyHostName"]
old-location: wmformat\iwmreadernetworkconfig_setproxyhostname.htm
tech.root: wmformat
ms.assetid: 5638a5d6-30f3-43eb-b054-cab85948796c
ms.date: 12/05/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetProxyHostName method, IWMReaderNetworkConfig.SetProxyHostName, IWMReaderNetworkConfig::SetProxyHostName, IWMReaderNetworkConfigSetProxyHostName, SetProxyHostName, SetProxyHostName method [windows Media Format], SetProxyHostName method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setproxyhostname, wmsdkidl/IWMReaderNetworkConfig::SetProxyHostName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMReaderNetworkConfig::SetProxyHostName
 - wmsdkidl/IWMReaderNetworkConfig::SetProxyHostName
dev_langs:
 - c++
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
 - IWMReaderNetworkConfig.SetProxyHostName
---

# IWMReaderNetworkConfig::SetProxyHostName


## -description

The <b>SetProxyHostName</b> method specifies the proxy host name.

## -parameters

### -param pwszProtocol [in]

Pointer to a wide-character <b>null</b>-terminated string containing the protocol.

### -param pwszHostName [in]

Pointer to a wide-character <b>null</b>-terminated string containing the host name. Host names are limited to 1024 wide characters.

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
<b>NULL</b> or invalid argument passed in.

</td>
</tr>
</table>

## -remarks

By default, the proxy host name is <b>NULL</b>, and must be set if a proxy is being used.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getproxyhostname">IWMReaderNetworkConfig::GetProxyHostName</a>