---
UID: NF:wmsdkidl.IWMStreamConfig.GetConnectionName
title: IWMStreamConfig::GetConnectionName (wmsdkidl.h)
description: The GetConnectionName method retrieves the input name given to the stream.
helpviewer_keywords: ["GetConnectionName","GetConnectionName method [windows Media Format]","GetConnectionName method [windows Media Format]","IWMStreamConfig interface","IWMStreamConfig interface [windows Media Format]","GetConnectionName method","IWMStreamConfig.GetConnectionName","IWMStreamConfig::GetConnectionName","IWMStreamConfigGetConnectionName","wmformat.iwmstreamconfig_getconnectionname","wmsdkidl/IWMStreamConfig::GetConnectionName"]
old-location: wmformat\iwmstreamconfig_getconnectionname.htm
tech.root: wmformat
ms.assetid: 04d50606-c355-45d4-9cc1-a8ef37113bf7
ms.date: 4/26/2023
ms.keywords: GetConnectionName, GetConnectionName method [windows Media Format], GetConnectionName method [windows Media Format],IWMStreamConfig interface, IWMStreamConfig interface [windows Media Format],GetConnectionName method, IWMStreamConfig.GetConnectionName, IWMStreamConfig::GetConnectionName, IWMStreamConfigGetConnectionName, wmformat.iwmstreamconfig_getconnectionname, wmsdkidl/IWMStreamConfig::GetConnectionName
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
 - IWMStreamConfig::GetConnectionName
 - wmsdkidl/IWMStreamConfig::GetConnectionName
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
 - IWMStreamConfig.GetConnectionName
---

# IWMStreamConfig::GetConnectionName


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetConnectionName</b> method retrieves the input name given to the stream.

## -parameters

### -param pwszInputName [out]

Pointer to a wide-character <b>null</b>-terminated string containing the input name. Pass <b>NULL</b> to retrieve the length of the name.

### -param pcchInputName [in, out]

On input, a pointer to a variable containing the length of the <i>pwszInputName</i> array in wide characters (2 bytes). On output, if the method succeeds, the variable contains the length of the name, including the terminating <b>null</b> character.

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
The <i>pcchInputName</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The name value contained in the <i>pcchInputName</i> parameter is too large for the <i>pwszInputName</i> array.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetConnectionName</b>. On the first call, pass <b>NULL</b> as <i>pwszInputName</i>. On return, the value pointed to by <i>pcchInputName</i> is set to the number of wide characters, including the terminating <b>null</b> character, required to hold the connection name. Then you can allocate the required amount of memory for the string and pass a pointer to it as <i>pwszInputName</i> on the second call.

The connection name is not written to the header section of an ASF file. If you obtain the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig</a> interface from the reader object or synchronous reader object, you cannot retrieve the original connection name.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig">IWMStreamConfig Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setconnectionname">IWMStreamConfig::SetConnectionName</a>