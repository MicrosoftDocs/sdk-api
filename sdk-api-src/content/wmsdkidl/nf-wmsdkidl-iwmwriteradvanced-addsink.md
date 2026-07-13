---
UID: NF:wmsdkidl.IWMWriterAdvanced.AddSink
title: IWMWriterAdvanced::AddSink (wmsdkidl.h)
description: The AddSink method adds a writer sink to receive writer output. The Windows Media Format SDK supports file sinks, which create ASF files on disk; network sinks, which stream ASF content across a network; and push sinks, which deliver ASF content to other media servers. To create a sink object, call one of the following functions:\_
helpviewer_keywords: ["AddSink","AddSink method [windows Media Format]","AddSink method [windows Media Format]","IWMWriterAdvanced interface","IWMWriterAdvanced interface [windows Media Format]","AddSink method","IWMWriterAdvanced.AddSink","IWMWriterAdvanced::AddSink","IWMWriterAdvancedAddSink","wmformat.iwmwriteradvanced_addsink","wmsdkidl/IWMWriterAdvanced::AddSink"]
old-location: wmformat\iwmwriteradvanced_addsink.htm
tech.root: wmformat
ms.assetid: 65763ac3-fba0-4de6-9c2e-4e241bbe5f13
ms.date: 4/26/2023
ms.keywords: AddSink, AddSink method [windows Media Format], AddSink method [windows Media Format],IWMWriterAdvanced interface, IWMWriterAdvanced interface [windows Media Format],AddSink method, IWMWriterAdvanced.AddSink, IWMWriterAdvanced::AddSink, IWMWriterAdvancedAddSink, wmformat.iwmwriteradvanced_addsink, wmsdkidl/IWMWriterAdvanced::AddSink
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
 - IWMWriterAdvanced::AddSink
 - wmsdkidl/IWMWriterAdvanced::AddSink
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
 - IWMWriterAdvanced.AddSink
---

# IWMWriterAdvanced::AddSink


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddSink</b> method adds a writer sink to receive writer output. The Windows Media Format SDK supports <i>file sinks</i>, which create ASF files on disk; <i>network sinks</i>, which stream ASF content across a network; and <i>push sinks</i>, which deliver ASF content to other media servers. To create a sink object, call one of the following functions:


<table>
<tr>
<th>Sink
          </th>
<th>Function
          </th>
</tr>
<tr>
<td>File sink</td>
<td>
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink">WMCreateWriterFileSink</a>
</td>
</tr>
<tr>
<td>Network sink</td>
<td>
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink">WMCreateWriterNetworkSink</a>
</td>
</tr>
<tr>
<td>Push sink</td>
<td>
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink">WMCreateWriterPushSink</a>
</td>
</tr>
</table> 

New sinks must be added to the writer with this method before they can be used.

## -parameters

### -param pSink [in]

Pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a> interface.

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
The <i>pSink</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The writer is not in a configurable state.

</td>
</tr>
</table>

## -remarks

If you only need to write to a single file, you can let the writer object handle the creation and management of a default file sink. To use a default file sink, pass a file name to the writer by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename">IWMWriter::SetOutputFilename</a>.

## -see-also

<a href="/windows/desktop/wmformat/adding-sinks-to-the-writer">Adding Sinks to the Writer</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink">IWMWriterAdvanced::GetSink</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink">IWMWriterAdvanced::RemoveSink</a>