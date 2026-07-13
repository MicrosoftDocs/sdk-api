---
UID: NF:wmsdkidl.IWMReaderNetworkConfig2.SetEnableContentCaching
title: IWMReaderNetworkConfig2::SetEnableContentCaching (wmsdkidl.h)
description: The SetEnableContentCaching method enables or disables content caching. If content caching is enabled, content that is being streamed can be cached locally.
helpviewer_keywords: ["IWMReaderNetworkConfig2 interface [windows Media Format]","SetEnableContentCaching method","IWMReaderNetworkConfig2.SetEnableContentCaching","IWMReaderNetworkConfig2::SetEnableContentCaching","IWMReaderNetworkConfig2SetEnableContentCaching","SetEnableContentCaching","SetEnableContentCaching method [windows Media Format]","SetEnableContentCaching method [windows Media Format]","IWMReaderNetworkConfig2 interface","wmformat.iwmreadernetworkconfig2_setenablecontentcaching","wmsdkidl/IWMReaderNetworkConfig2::SetEnableContentCaching"]
old-location: wmformat\iwmreadernetworkconfig2_setenablecontentcaching.htm
tech.root: wmformat
ms.assetid: 68dcb12e-e254-407e-864b-54d4e84b08ed
ms.date: 4/26/2023
ms.keywords: IWMReaderNetworkConfig2 interface [windows Media Format],SetEnableContentCaching method, IWMReaderNetworkConfig2.SetEnableContentCaching, IWMReaderNetworkConfig2::SetEnableContentCaching, IWMReaderNetworkConfig2SetEnableContentCaching, SetEnableContentCaching, SetEnableContentCaching method [windows Media Format], SetEnableContentCaching method [windows Media Format],IWMReaderNetworkConfig2 interface, wmformat.iwmreadernetworkconfig2_setenablecontentcaching, wmsdkidl/IWMReaderNetworkConfig2::SetEnableContentCaching
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMReaderNetworkConfig2::SetEnableContentCaching
 - wmsdkidl/IWMReaderNetworkConfig2::SetEnableContentCaching
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
 - IWMReaderNetworkConfig2.SetEnableContentCaching
---

# IWMReaderNetworkConfig2::SetEnableContentCaching


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetEnableContentCaching</b> method enables or disables content caching. If content caching is enabled, content that is being streamed can be cached locally.

## -parameters

### -param fEnableContentCaching [in]

Boolean value that is True to enable content caching.

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
</table>

## -remarks

This method applies only to content being streamed from a server running Windows Media Services.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2">IWMReaderNetworkConfig2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-getenablecontentcaching">IWMReaderNetworkConfig2::GetEnableContentCaching</a>