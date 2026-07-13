---
UID: NF:wmsdkidl.IWMMetadataEditor.Flush
title: IWMMetadataEditor::Flush (wmsdkidl.h)
description: The Flush method closes the open file, saving any changes.
helpviewer_keywords: ["Flush","Flush method [windows Media Format]","Flush method [windows Media Format]","IWMMetadataEditor interface","IWMMetadataEditor interface [windows Media Format]","Flush method","IWMMetadataEditor.Flush","IWMMetadataEditor::Flush","IWMMetadataEditorFlush","wmformat.iwmmetadataeditor_flush","wmsdkidl/IWMMetadataEditor::Flush"]
old-location: wmformat\iwmmetadataeditor_flush.htm
tech.root: wmformat
ms.assetid: b17992f7-ed93-4f62-bf50-8fb2fd41caee
ms.date: 4/26/2023
ms.keywords: Flush, Flush method [windows Media Format], Flush method [windows Media Format],IWMMetadataEditor interface, IWMMetadataEditor interface [windows Media Format],Flush method, IWMMetadataEditor.Flush, IWMMetadataEditor::Flush, IWMMetadataEditorFlush, wmformat.iwmmetadataeditor_flush, wmsdkidl/IWMMetadataEditor::Flush
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
 - IWMMetadataEditor::Flush
 - wmsdkidl/IWMMetadataEditor::Flush
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
 - IWMMetadataEditor.Flush
---

# IWMMetadataEditor::Flush


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Flush</b> method closes the open file, saving any changes.



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
<dt><b>ASF_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
No file has been opened.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_FILE_WRITE</b></dt>
</dl>
</td>
<td width="60%">
Read-only file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor">IWMMetadataEditor Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmetadataeditor-close">IWMMetadataEditor::Close</a>
