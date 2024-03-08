---
UID: NF:wmsdkidl.IWMDRMTranscryptor.Seek
title: IWMDRMTranscryptor::Seek (wmsdkidl.h)
description: The Seek method sets the DRM transcryptor to read from the specified point in the data stream of the loaded file. Subsequent Read calls generate data beginning at that point.
helpviewer_keywords: ["IWMDRMTranscryptor interface [windows Media Format]","Seek method","IWMDRMTranscryptor.Seek","IWMDRMTranscryptor::Seek","IWMDRMTranscryptorSeek","Seek","Seek method [windows Media Format]","Seek method [windows Media Format]","IWMDRMTranscryptor interface","wmformat.iwmdrmtranscryptor_seek","wmsdkidl/IWMDRMTranscryptor::Seek"]
old-location: wmformat\iwmdrmtranscryptor_seek.htm
tech.root: wmformat
ms.assetid: 4962741b-d1ca-4296-ad95-d171d165c5d9
ms.date: 4/26/2023
ms.keywords: IWMDRMTranscryptor interface [windows Media Format],Seek method, IWMDRMTranscryptor.Seek, IWMDRMTranscryptor::Seek, IWMDRMTranscryptorSeek, Seek, Seek method [windows Media Format], Seek method [windows Media Format],IWMDRMTranscryptor interface, wmformat.iwmdrmtranscryptor_seek, wmsdkidl/IWMDRMTranscryptor::Seek
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
 - IWMDRMTranscryptor::Seek
 - wmsdkidl/IWMDRMTranscryptor::Seek
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
 - IWMDRMTranscryptor.Seek
---

# IWMDRMTranscryptor::Seek


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>Seek</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>Seek</b> method sets the DRM transcryptor to read from the specified point in the data stream of the loaded file. Subsequent <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read">Read</a> calls generate data beginning at that point.

## -parameters

### -param hnsTime [in]

Seek time in 100-nanosecond units.

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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
There is no file loaded in the transcryptor.

</td>
</tr>
</table>

## -remarks

This method is asynchronous. It returns immediately, but processing is not complete until a WMT_TRANSCRYPTOR_SEEKED message is sent to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> callback method.

If the seek operation fails, no message is sent.

The first successful call to <b>Seek</b> causes the transcryptor to read the ASF header for the content. All subsequent <b>Seek</b> calls change the reading location in the data section, but do not generate a header or an ASF Data Object (the ASF object that contains top-level information about the data section).

To convert the entire file, call <b>Seek</b> with a presentation time of 0.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor">IWMDRMTranscryptor Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmtranscryptor-read">IWMDRMTranscryptor::Read</a>