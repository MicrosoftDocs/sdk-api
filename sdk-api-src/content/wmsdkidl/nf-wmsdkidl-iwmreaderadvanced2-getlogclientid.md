---
UID: NF:wmsdkidl.IWMReaderAdvanced2.GetLogClientID
title: IWMReaderAdvanced2::GetLogClientID (wmsdkidl.h)
description: The GetLogClientID method queries whether the reader logs the client's unique ID or an anonymous session ID.
helpviewer_keywords: ["GetLogClientID","GetLogClientID method [windows Media Format]","GetLogClientID method [windows Media Format]","IWMReaderAdvanced2 interface","IWMReaderAdvanced2 interface [windows Media Format]","GetLogClientID method","IWMReaderAdvanced2.GetLogClientID","IWMReaderAdvanced2::GetLogClientID","IWMReaderAdvanced2GetLogClientID","wmformat.iwmreaderadvanced2_getlogclientid","wmsdkidl/IWMReaderAdvanced2::GetLogClientID"]
old-location: wmformat\iwmreaderadvanced2_getlogclientid.htm
tech.root: wmformat
ms.assetid: 034ad344-2266-4662-9797-70031f58f0cd
ms.date: 4/26/2023
ms.keywords: GetLogClientID, GetLogClientID method [windows Media Format], GetLogClientID method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced2 interface [windows Media Format],GetLogClientID method, IWMReaderAdvanced2.GetLogClientID, IWMReaderAdvanced2::GetLogClientID, IWMReaderAdvanced2GetLogClientID, wmformat.iwmreaderadvanced2_getlogclientid, wmsdkidl/IWMReaderAdvanced2::GetLogClientID
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
 - IWMReaderAdvanced2::GetLogClientID
 - wmsdkidl/IWMReaderAdvanced2::GetLogClientID
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
 - IWMReaderAdvanced2.GetLogClientID
---

# IWMReaderAdvanced2::GetLogClientID


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetLogClientID</b> method queries whether the reader logs the client's unique ID or an anonymous session ID.

## -parameters

### -param pfLogClientID [out]

Pointer Boolean value that is set to True if the client's log ID must be sent to the server.

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
A <b>NULL</b> or invalid argument was passed in.

</td>
</tr>
</table>

## -remarks

See the remarks for <b>SetLogClientID</b>.

## -see-also

<a href="/windows/desktop/wmformat/client">Client Logging</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid">IWMReaderAdvanced2::SetLogClientID</a>