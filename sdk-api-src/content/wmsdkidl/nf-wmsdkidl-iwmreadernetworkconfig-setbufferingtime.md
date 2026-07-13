---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.SetBufferingTime
title: IWMReaderNetworkConfig::SetBufferingTime (wmsdkidl.h)
description: The SetBufferingTime method specifies how long the network source buffers data before rendering it.
helpviewer_keywords: ["IWMReaderNetworkConfig interface [windows Media Format]","SetBufferingTime method","IWMReaderNetworkConfig.SetBufferingTime","IWMReaderNetworkConfig::SetBufferingTime","IWMReaderNetworkConfigSetBufferingTime","SetBufferingTime","SetBufferingTime method [windows Media Format]","SetBufferingTime method [windows Media Format]","IWMReaderNetworkConfig interface","wmformat.iwmreadernetworkconfig_setbufferingtime","wmsdkidl/IWMReaderNetworkConfig::SetBufferingTime"]
old-location: wmformat\iwmreadernetworkconfig_setbufferingtime.htm
tech.root: wmformat
ms.assetid: 64b8eb13-3b96-4bb7-8d75-0eccb1af5a2f
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig interface [windows Media Format],SetBufferingTime method, IWMReaderNetworkConfig.SetBufferingTime, IWMReaderNetworkConfig::SetBufferingTime, IWMReaderNetworkConfigSetBufferingTime, SetBufferingTime, SetBufferingTime method [windows Media Format], SetBufferingTime method [windows Media Format],IWMReaderNetworkConfig interface, wmformat.iwmreadernetworkconfig_setbufferingtime, wmsdkidl/IWMReaderNetworkConfig::SetBufferingTime
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
 - IWMReaderNetworkConfig::SetBufferingTime
 - wmsdkidl/IWMReaderNetworkConfig::SetBufferingTime
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
 - IWMReaderNetworkConfig.SetBufferingTime
---

# IWMReaderNetworkConfig::SetBufferingTime


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetBufferingTime</b> method specifies how long the network source buffers data before rendering it.

## -parameters

### -param cnsBufferingTime [in]

Specifies the amount of time in to buffer content before starting playback, in 100-nanosecond units.

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
<i>cnsBufferingTime</i> is larger than the maximum or smaller than the minimum.

</td>
</tr>
</table>

## -remarks

The minimum buffering time is 1 second and the maximum is 60 seconds. To set a buffering time of 1 second, for example, set the value to 10000000.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getbufferingtime">IWMReaderNetworkConfig::GetBufferingTime</a>