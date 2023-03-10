---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetEnableTCP
title: IWMReaderNetworkConfig::SetEnableTCP (wmsdkidl.h)
description: The SetEnableTCP method enables or disables TCP.
helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","SetEnableTCP method","IWMReaderNetworkConfig.SetEnableTCP","IWMReaderNetworkConfig::SetEnableTCP","IWMReaderNetworkConfigSetEnableTCP","SetEnableTCP","SetEnableTCP method [windows Media Format]","SetEnableTCP method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_setenabletcp","wmsdkidl/IWMReaderNetworkConfig::SetEnableTCP"]
old-location: wmformat\iwmreadernetworkconfig_setenabletcp.htm
tech.root: wmformat
ms.assetid: 8afc62b8-a2f6-4470-8005-804e0980b599
ms.date: 12/05/2018
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetEnableTCP method, IWMReaderNetworkConfig.SetEnableTCP, IWMReaderNetworkConfig::SetEnableTCP, IWMReaderNetworkConfigSetEnableTCP, SetEnableTCP, SetEnableTCP method [windows Media Format], SetEnableTCP method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setenabletcp, wmsdkidl/IWMReaderNetworkConfig::SetEnableTCP
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
 - IWMReaderNetworkConfig::SetEnableTCP
 - wmsdkidl/IWMReaderNetworkConfig::SetEnableTCP
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
 - IWMReaderNetworkConfig.SetEnableTCP
---

# IWMReaderNetworkConfig::SetEnableTCP


## -description

The <b>SetEnableTCP</b> method enables or disables TCP.

## -parameters

### -param fEnableTCP [in]

Boolean value that is True if TCP is to be enabled. Set this to true if the SDK can use TCP-based MMS streaming when selecting a protocol for streaming.

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

This setting applies only to a protocol rollover or MMS://URL. Even if this setting is disabled, the application can still specify an explicit MMST://URL and stream MMS via TCP successfully.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getenabletcp">IWMReaderNetworkConfig::GetEnableTCP</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getenableudp">IWMReaderNetworkConfig::GetEnableUDP</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setenableudp">IWMReaderNetworkConfig::SetEnableUDP</a>