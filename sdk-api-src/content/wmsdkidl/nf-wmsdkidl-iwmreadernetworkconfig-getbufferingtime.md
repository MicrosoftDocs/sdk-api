---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetBufferingTime
title: IWMReaderNetworkConfig::GetBufferingTime (wmsdkidl.h)
description: The GetBufferingTime method retrieves the amount of time that the network source buffers data before rendering it.
helpviewer_keywords: ["GetBufferingTime","GetBufferingTime method [windows Media Format]","GetBufferingTime method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetBufferingTime method","IWMReaderNetworkConfig.GetBufferingTime","IWMReaderNetworkConfig::GetBufferingTime","IWMReaderNetworkConfigGetBufferingTime","wmformat.iwmreadernetworkconfig_getbufferingtime","wmsdkidl/IWMReaderNetworkConfig::GetBufferingTime"]
old-location: wmformat\iwmreadernetworkconfig_getbufferingtime.htm
tech.root: wmformat
ms.assetid: a3f35230-363c-48e7-bef9-b92e0b50b978
ms.date: 12/05/2018
ms.keywords: GetBufferingTime, GetBufferingTime method [windows Media Format], GetBufferingTime method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetBufferingTime method, IWMReaderNetworkConfig.GetBufferingTime, IWMReaderNetworkConfig::GetBufferingTime, IWMReaderNetworkConfigGetBufferingTime, wmformat.iwmreadernetworkconfig_getbufferingtime, wmsdkidl/IWMReaderNetworkConfig::GetBufferingTime
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
 - IWMReaderNetworkConfig::GetBufferingTime
 - wmsdkidl/IWMReaderNetworkConfig::GetBufferingTime
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
 - IWMReaderNetworkConfig.GetBufferingTime
---

# IWMReaderNetworkConfig::GetBufferingTime


## -description

The <b>GetBufferingTime</b> method retrieves the amount of time that the network source buffers data before rendering it.

## -parameters

### -param pcnsBufferingTime [out]

Pointer to a variable that receives the buffering time, in 100-nanosecond units.

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
NULL passed in to <i>pcnsBufferingTime</i>

</td>
</tr>
</table>

## -remarks

See the Remarks for <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setbufferingtime">SetBufferingTime</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setbufferingtime">IWMReaderNetworkConfig::SetBufferingTime</a>