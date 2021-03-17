---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetForceRerunAutoProxyDetection
title: IWMReaderNetworkConfig::GetForceRerunAutoProxyDetection (wmsdkidl.h)
description: The GetForceRerunAutoProxyDetection method ascertains whether forced rerun detection is enabled.
helpviewer_keywords: ["GetForceRerunAutoProxyDetection","GetForceRerunAutoProxyDetection method [windows Media Format]","GetForceRerunAutoProxyDetection method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetForceRerunAutoProxyDetection method","IWMReaderNetworkConfig.GetForceRerunAutoProxyDetection","IWMReaderNetworkConfig::GetForceRerunAutoProxyDetection","IWMReaderNetworkConfigGetForceRerunAutoProxyDetection","wmformat.iwmreadernetworkconfig_getforcererunautoproxydetection","wmsdkidl/IWMReaderNetworkConfig::GetForceRerunAutoProxyDetection"]
old-location: wmformat\iwmreadernetworkconfig_getforcererunautoproxydetection.htm
tech.root: wmformat
ms.assetid: af4c4f4d-ad19-46b5-b38f-9aa51f2d95ba
ms.date: 12/05/2018
ms.keywords: GetForceRerunAutoProxyDetection, GetForceRerunAutoProxyDetection method [windows Media Format], GetForceRerunAutoProxyDetection method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetForceRerunAutoProxyDetection method, IWMReaderNetworkConfig.GetForceRerunAutoProxyDetection, IWMReaderNetworkConfig::GetForceRerunAutoProxyDetection, IWMReaderNetworkConfigGetForceRerunAutoProxyDetection, wmformat.iwmreadernetworkconfig_getforcererunautoproxydetection, wmsdkidl/IWMReaderNetworkConfig::GetForceRerunAutoProxyDetection
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
 - IWMReaderNetworkConfig::GetForceRerunAutoProxyDetection
 - wmsdkidl/IWMReaderNetworkConfig::GetForceRerunAutoProxyDetection
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
 - IWMReaderNetworkConfig.GetForceRerunAutoProxyDetection
---

# IWMReaderNetworkConfig::GetForceRerunAutoProxyDetection


## -description

The <b>GetForceRerunAutoProxyDetection</b> method ascertains whether forced rerun detection is enabled.

## -parameters

### -param pfForceRerunDetection [out]

Pointer to a Boolean value that is set to True if forced rerun detection has been enabled.

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

See the Remarks for <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setforcererunautoproxydetection">SetForceRerunAutoProxyDetection</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setforcererunautoproxydetection">IWMReaderNetworkConfig::SetForceRerunAutoProxyDetection</a>