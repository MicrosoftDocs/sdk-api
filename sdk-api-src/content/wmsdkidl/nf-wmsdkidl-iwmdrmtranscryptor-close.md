---
UID: NF:wmsdkidl.IWMDRMTranscryptor.Close
title: IWMDRMTranscryptor::Close (wmsdkidl.h)
description: The Close method unloads the file from the DRM transcryptor and releases all associated resources.
helpviewer_keywords: ["Close","Close method [windows Media Format]","Close method [windows Media Format]","IWMDRMTranscryptor interface","IWMDRMTranscryptor interface [windows Media Format]","Close method","IWMDRMTranscryptor.Close","IWMDRMTranscryptor::Close","IWMDRMTranscryptorClose","wmformat.iwmdrmtranscryptor_close","wmsdkidl/IWMDRMTranscryptor::Close"]
old-location: wmformat\iwmdrmtranscryptor_close.htm
tech.root: wmformat
ms.assetid: c277e3fa-069d-4eaf-947c-220730c5d61e
ms.date: 4/26/2023
ms.keywords: Close, Close method [windows Media Format], Close method [windows Media Format],IWMDRMTranscryptor interface, IWMDRMTranscryptor interface [windows Media Format],Close method, IWMDRMTranscryptor.Close, IWMDRMTranscryptor::Close, IWMDRMTranscryptorClose, wmformat.iwmdrmtranscryptor_close, wmsdkidl/IWMDRMTranscryptor::Close
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDRMTranscryptor::Close
 - wmsdkidl/IWMDRMTranscryptor::Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMDRMTranscryptor.Close
---

# IWMDRMTranscryptor::Close


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>Close</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>Close</b> method unloads the file from the DRM transcryptor and releases all associated resources.



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

This method is asynchronous. It returns immediately, but processing is not complete until a WMT_TRANSCRYPTOR_CLOSED message is sent to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> callback method.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor">IWMDRMTranscryptor Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-initialize">IWMDRMTranscryptor::Initialize</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read">IWMDRMTranscryptor::Read</a>
