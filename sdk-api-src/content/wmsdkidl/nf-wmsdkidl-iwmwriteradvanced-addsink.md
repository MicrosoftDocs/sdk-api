---
UID: NF:wmsdkidl.IWMWriterAdvanced.AddSink
title: IWMWriterAdvanced::AddSink (wmsdkidl.h)
description: The AddSink method adds a writer sink to receive writer output. The Windows Media Format SDK supports file sinks, which create ASF files on disk; network sinks, which stream ASF content across a network; and push sinks, which deliver ASF content to other media servers. To create a sink object, call one of the following functions:\_helpviewer_keywords: ["AddSink","AddSink method [windows Media Format]","AddSink method [windows Media Format]","IWMWriterAdvanced interface","IWMWriterAdvanced interface [windows Media Format]","AddSink method","IWMWriterAdvanced.AddSink","IWMWriterAdvanced::AddSink","IWMWriterAdvancedAddSink","wmformat.iwmwriteradvanced_addsink","wmsdkidl/IWMWriterAdvanced::AddSink"]
The AddSink method adds a writer sink to receive writer output. The Windows Media Format SDK supports file sinks, which create ASF files on disk; network sinks, which stream ASF content across a network; and push sinks, which deliver ASF content to other media servers. To create a sink object, call one of the following functions: New sinks must be added to the writer with this method before they can be used.
old-location: wmformat\iwmwriteradvanced_addsink.htm
tech.root: wmformat
ms.assetid: 65763ac3-fba0-4de6-9c2e-4e241bbe5f13
ms.date: 12/05/2018
ms.keywords: AddSink, AddSink method [windows Media Format], AddSink method [windows Media Format],IWMWriterAdvanced interface, IWMWriterAdvanced interface [windows Media Format],AddSink method, IWMWriterAdvanced.AddSink, IWMWriterAdvanced::AddSink, IWMWriterAdvancedAddSink, wmformat.iwmwriteradvanced_addsink, wmsdkidl/IWMWriterAdvanced::AddSink
f1_keywords: 
 - "wmsdkidl/IWMWriterAdvanced.AddSink"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterAdvanced::AddSink


## -description



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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink">WMCreateWriterFileSink</a>
</td>
</tr>
<tr>
<td>Network sink</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink">WMCreateWriterNetworkSink</a>
</td>
</tr>
<tr>
<td>Push sink</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink">WMCreateWriterPushSink</a>
</td>
</tr>
</table> 

New sinks must be added to the writer with this method before they can be used.


## -parameters




### -param pSink [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a> interface.


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



If you only need to write to a single file, you can let the writer object handle the creation and management of a default file sink. To use a default file sink, pass a file name to the writer by calling <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename">IWMWriter::SetOutputFilename</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/adding-sinks-to-the-writer">Adding Sinks to the Writer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink">IWMWriterAdvanced::GetSink</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink">IWMWriterAdvanced::RemoveSink</a>
 

 

