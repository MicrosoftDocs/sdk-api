---
UID: NF:wmsdkidl.IWMWriterAdvanced.GetSinkCount
title: IWMWriterAdvanced::GetSinkCount (wmsdkidl.h)
description: The GetSinkCount method retrieves the number of writer sinks associated with the writer object.
helpviewer_keywords: ["GetSinkCount","GetSinkCount method [windows Media Format]","GetSinkCount method [windows Media Format]","IWMWriterAdvanced interface","IWMWriterAdvanced interface [windows Media Format]","GetSinkCount method","IWMWriterAdvanced.GetSinkCount","IWMWriterAdvanced::GetSinkCount","IWMWriterAdvancedGetSinkCount","wmformat.iwmwriteradvanced_getsinkcount","wmsdkidl/IWMWriterAdvanced::GetSinkCount"]
old-location: wmformat\iwmwriteradvanced_getsinkcount.htm
tech.root: wmformat
ms.assetid: 210c96bc-3659-43e6-acb2-4d9f328e81e0
ms.date: 4/26/2023
ms.keywords: GetSinkCount, GetSinkCount method [windows Media Format], GetSinkCount method [windows Media Format],IWMWriterAdvanced interface, IWMWriterAdvanced interface [windows Media Format],GetSinkCount method, IWMWriterAdvanced.GetSinkCount, IWMWriterAdvanced::GetSinkCount, IWMWriterAdvancedGetSinkCount, wmformat.iwmwriteradvanced_getsinkcount, wmsdkidl/IWMWriterAdvanced::GetSinkCount
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
 - IWMWriterAdvanced::GetSinkCount
 - wmsdkidl/IWMWriterAdvanced::GetSinkCount
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
 - IWMWriterAdvanced.GetSinkCount
---

# IWMWriterAdvanced::GetSinkCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetSinkCount</b> method retrieves the number of writer sinks associated with the writer object. To obtain a pointer to an interface of an individual sink, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink">IWMWriterAdvanced::GetSink</a> using a sink number between 0 and one less than the count returned by this method.

## -parameters

### -param pcSinks [out]

DWORD indicating the total number of sinks associated with the writer object.

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
<i>pcSinks</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

If you specify a file by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename">IWMWriter::SetOutputFilename</a>, the writer object will automatically create a file sink and add it to the writer. That sink will be included in the count retrieved by this method.

## -see-also

<a href="/windows/desktop/wmformat/enumerating-sinks">Enumerating Sinks</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink">IWMWriterAdvanced::GetSink</a>