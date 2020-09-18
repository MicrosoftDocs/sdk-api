---
UID: NF:wmsdkidl.IWMWriterAdvanced.RemoveSink
title: IWMWriterAdvanced::RemoveSink (wmsdkidl.h)
description: The RemoveSink method removes a writer sink object.
helpviewer_keywords: ["IWMWriterAdvanced interface [windows Media Format]","RemoveSink method","IWMWriterAdvanced.RemoveSink","IWMWriterAdvanced::RemoveSink","IWMWriterAdvancedRemoveSink","RemoveSink","RemoveSink method [windows Media Format]","RemoveSink method [windows Media Format]","IWMWriterAdvanced interface","wmformat.iwmwriteradvanced_removesink","wmsdkidl/IWMWriterAdvanced::RemoveSink"]
old-location: wmformat\iwmwriteradvanced_removesink.htm
tech.root: wmformat
ms.assetid: e2fc7f82-981a-4f69-b99d-71514ed2c6ae
ms.date: 12/05/2018
ms.keywords: IWMWriterAdvanced interface [windows Media Format],RemoveSink method, IWMWriterAdvanced.RemoveSink, IWMWriterAdvanced::RemoveSink, IWMWriterAdvancedRemoveSink, RemoveSink, RemoveSink method [windows Media Format], RemoveSink method [windows Media Format],IWMWriterAdvanced interface, wmformat.iwmwriteradvanced_removesink, wmsdkidl/IWMWriterAdvanced::RemoveSink
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
 - IWMWriterAdvanced::RemoveSink
 - wmsdkidl/IWMWriterAdvanced::RemoveSink
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
 - IWMWriterAdvanced.RemoveSink
---

# IWMWriterAdvanced::RemoveSink


## -description

The <b>RemoveSink</b> method removes a writer sink object.

## -parameters

### -param pSink [in]

Pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink">IWMWriterSink</a> interface of the sink object to remove, or <b>NULL</b> to remove all sinks.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Could not remove the specified sink.

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

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink">IWMWriterAdvanced::AddSink</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink">IWMWriterAdvanced::GetSink</a>