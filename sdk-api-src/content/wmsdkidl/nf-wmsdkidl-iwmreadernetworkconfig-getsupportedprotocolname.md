---
UID: NF:wmsdkidl.IWMReaderNetworkConfig.GetSupportedProtocolName
title: IWMReaderNetworkConfig::GetSupportedProtocolName (wmsdkidl.h)
description: The GetSupportedProtocolName method retrieves a protocol name by index.
helpviewer_keywords: ["GetSupportedProtocolName","GetSupportedProtocolName method [windows Media Format]","GetSupportedProtocolName method [windows Media Format]","IWMReaderNetworkConfig interface","IWMReaderNetworkConfig interface [windows Media Format]","GetSupportedProtocolName method","IWMReaderNetworkConfig.GetSupportedProtocolName","IWMReaderNetworkConfig::GetSupportedProtocolName","IWMReaderNetworkConfigGetSupportedProtocolName","wmformat.iwmreadernetworkconfig_getsupportedprotocolname","wmsdkidl/IWMReaderNetworkConfig::GetSupportedProtocolName"]
old-location: wmformat\iwmreadernetworkconfig_getsupportedprotocolname.htm
tech.root: wmformat
ms.assetid: c1047752-c3a2-4555-9dae-ddd91365cd10
ms.date: 4/26/2023
ms.keywords: GetSupportedProtocolName, GetSupportedProtocolName method [windows Media Format], GetSupportedProtocolName method [windows Media Format],IWMReaderNetworkConfig interface, IWMReaderNetworkConfig interface [windows Media Format],GetSupportedProtocolName method, IWMReaderNetworkConfig.GetSupportedProtocolName, IWMReaderNetworkConfig::GetSupportedProtocolName, IWMReaderNetworkConfigGetSupportedProtocolName, wmformat.iwmreadernetworkconfig_getsupportedprotocolname, wmsdkidl/IWMReaderNetworkConfig::GetSupportedProtocolName
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
 - IWMReaderNetworkConfig::GetSupportedProtocolName
 - wmsdkidl/IWMReaderNetworkConfig::GetSupportedProtocolName
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
 - IWMReaderNetworkConfig.GetSupportedProtocolName
---

# IWMReaderNetworkConfig::GetSupportedProtocolName


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetSupportedProtocolName</b> method retrieves a protocol name by index.

## -parameters

### -param dwProtocolNum [in]

Specifies protocol name to retrieve, indexed from zero. To get the number of supported protocols, call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getnumprotocolssupported">IWMReaderNetworkConfig::GetNumProtocolsSupported</a> method.

### -param pwszProtocolName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the protocol name. Pass <b>NULL</b> to retrieve the length of the name.

### -param pcchProtocolName [in, out]

On input, pointer to a <b>DWORD</b> containing the length of the <i>pwszProtocolName</i>, in characters. On output, pointer to the length of the protocol name, including the terminating <b>null</b> character.

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

You should make two calls to <b>GetSupportedProtocolName</b>. On the first call, pass <b>NULL</b> for <i>pwszProtocoName</i>. On return, the value pointed to by <i>pcchProtocolName</i> is set to the number of wide characters, including the terminating <b>null</b>, required to hold the protocol name. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszProtocolName</i> on the second call.

Use this method along with <b>GetNumProtocolsSupported</b> to iterate through the network protocols supported by the reader object.

This method only returns a list of protocols that are used to receive content from Windows Media servers. Protocols that are only used for retrieving content from local sources, or non-Windows Media servers (such as Web servers) are not included in this list.

<div class="alert"><b>Note</b>  The HTTPS support works only when downloading content from a Web server (because the player is using WININET). Streaming protocols supported are HTTP, RTSP, MMS, and, for multicasting, ASFM (by opening an ASF file with an .nsc extension). Download support includes HTTP, HTTPS, and FTP.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig">IWMReaderNetworkConfig Interface</a>