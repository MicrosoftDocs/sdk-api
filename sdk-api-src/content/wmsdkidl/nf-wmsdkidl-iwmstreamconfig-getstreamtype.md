---
UID: NF:wmsdkidl.IWMStreamConfig.GetStreamType
title: IWMStreamConfig::GetStreamType (wmsdkidl.h)
description: The GetStreamType method retrieves the major type of the stream (audio, video, or script).
helpviewer_keywords: ["GetStreamType","GetStreamType method [windows Media Format]","GetStreamType method [windows Media Format]","IWMStreamConfig interface","IWMStreamConfig interface [windows Media Format]","GetStreamType method","IWMStreamConfig.GetStreamType","IWMStreamConfig::GetStreamType","IWMStreamConfigGetStreamType","wmformat.iwmstreamconfig_getstreamtype","wmsdkidl/IWMStreamConfig::GetStreamType"]
old-location: wmformat\iwmstreamconfig_getstreamtype.htm
tech.root: wmformat
ms.assetid: a8dc8c37-da52-4d0f-b143-aaa45e6f77b8
ms.date: 4/26/2023
ms.keywords: GetStreamType, GetStreamType method [windows Media Format], GetStreamType method [windows Media Format],IWMStreamConfig interface, IWMStreamConfig interface [windows Media Format],GetStreamType method, IWMStreamConfig.GetStreamType, IWMStreamConfig::GetStreamType, IWMStreamConfigGetStreamType, wmformat.iwmstreamconfig_getstreamtype, wmsdkidl/IWMStreamConfig::GetStreamType
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
 - IWMStreamConfig::GetStreamType
 - wmsdkidl/IWMStreamConfig::GetStreamType
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
 - IWMStreamConfig.GetStreamType
---

# IWMStreamConfig::GetStreamType


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetStreamType</b> method retrieves the major type of the stream (audio, video, or script).

## -parameters

### -param pguidStreamType [out]

Pointer to a GUID object specifying the major type of the stream. Receives the value GUID_NULL if the *pMediaType* parameter is NULL.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pguidStreamType</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

For a table of stream major types, see <a href="/windows/desktop/wmformat/media-types">Media Types</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getstreamname">IWMStreamConfig::GetStreamName</a>
