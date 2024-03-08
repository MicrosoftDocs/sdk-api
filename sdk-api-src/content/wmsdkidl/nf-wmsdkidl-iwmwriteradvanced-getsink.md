---
UID: NF:wmsdkidl.IWMWriterAdvanced.GetSink
title: IWMWriterAdvanced::GetSink (wmsdkidl.h)
description: The GetSink method retrieves a writer sink object. Used in conjunction with IWMWriterAdvanced::GetSinkCount, this method can be used to enumerate the sinks associated with a writer object.
helpviewer_keywords: ["GetSink","GetSink method [windows Media Format]","GetSink method [windows Media Format]","IWMWriterAdvanced interface","IWMWriterAdvanced interface [windows Media Format]","GetSink method","IWMWriterAdvanced.GetSink","IWMWriterAdvanced::GetSink","IWMWriterAdvancedGetSink","wmformat.iwmwriteradvanced_getsink","wmsdkidl/IWMWriterAdvanced::GetSink"]
old-location: wmformat\iwmwriteradvanced_getsink.htm
tech.root: wmformat
ms.assetid: 6775eb89-a3af-42d2-b1e3-197abb1fce61
ms.date: 4/26/2023
ms.keywords: GetSink, GetSink method [windows Media Format], GetSink method [windows Media Format],IWMWriterAdvanced interface, IWMWriterAdvanced interface [windows Media Format],GetSink method, IWMWriterAdvanced.GetSink, IWMWriterAdvanced::GetSink, IWMWriterAdvancedGetSink, wmformat.iwmwriteradvanced_getsink, wmsdkidl/IWMWriterAdvanced::GetSink
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
 - IWMWriterAdvanced::GetSink
 - wmsdkidl/IWMWriterAdvanced::GetSink
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
 - IWMWriterAdvanced.GetSink
---

# IWMWriterAdvanced::GetSink


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetSink</b> method retrieves a writer sink object. Used in conjunction with <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount">IWMWriterAdvanced::GetSinkCount</a>, this method can be used to enumerate the sinks associated with a writer object.

## -parameters

### -param dwSinkNum [in]

<b>DWORD</b> containing the sink number (its index). This is a number between 0 and one less than the total number of sinks associated with the file as obtained with <b>IWMWriterAdvanced::GetSinkCount</b>.

### -param ppSink [out]

Pointer to a pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a> interface.

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
Either the <i>ppSink</i> parameter is <b>NULL</b>, or the <i>dwSinkNum</i> parameter is greater than the number of sinks.

</td>
</tr>
</table>

## -remarks

You can use <b>GetSink</b> to gain access to the file sink that is automatically created when you call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename">IWMWriter::SetOutputFilename</a>. If you are only writing to the automatically created file sink, it will always be sink number 0.

## -see-also

<a href="/windows/desktop/wmformat/enumerating-sinks">Enumerating Sinks</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink">IWMWriterAdvanced::AddSink</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount">IWMWriterAdvanced::GetSinkCount</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink">IWMWriterAdvanced::RemoveSink</a>