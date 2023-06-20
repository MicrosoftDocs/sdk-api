---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetForceRerunAutoProxyDetection
title: IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection (wmsdkidl.h)
description: The SetForceRerunAutoProxyDetection method enables or disables forced rerun detection.
helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","SetForceRerunAutoProxyDetection method","IWMReaderNetworkConfig.SetForceRerunAutoProxyDetection","IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection","IWMReaderNetworkConfigSetForceRerunAutoProxyDetection","SetForceRerunAutoProxyDetection","SetForceRerunAutoProxyDetection method [windows Media Format]","SetForceRerunAutoProxyDetection method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_setforcererunautoproxydetection","wmsdkidl/IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection"]
old-location: wmformat\iwmreadernetworkconfig_setforcererunautoproxydetection.htm
tech.root: wmformat
ms.assetid: 3c84fc2a-5933-45da-a7a3-728a8837d851
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetForceRerunAutoProxyDetection method, IWMReaderNetworkConfig.SetForceRerunAutoProxyDetection, IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection, IWMReaderNetworkConfigSetForceRerunAutoProxyDetection, SetForceRerunAutoProxyDetection, SetForceRerunAutoProxyDetection method [windows Media Format], SetForceRerunAutoProxyDetection method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setforcererunautoproxydetection, wmsdkidl/IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection
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
 - IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection
 - wmsdkidl/IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection
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
 - IWMReaderNetworkConfig.SetForceRerunAutoProxyDetection
---

# IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetForceRerunAutoProxyDetection</b> method enables or disables forced rerun detection.

## -parameters

### -param fForceRerunDetection [in]

Boolean value that is True if forced rerun detection is to be enabled.

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

Forced rerun detection indicates that Web Proxy Auto-Detection mechanisms must be invoked before the next streaming connection is established.

Setting <i>fForceRerunDetection</i> to True applies to all protocols when the auto setting has been specified by the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setproxysettings">SetProxySettings</a> method.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getforcererunautoproxydetection">IWMReaderNetworkConfig::GetForceRerunAutoProxyDetection</a>