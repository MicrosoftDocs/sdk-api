---
UID: NF:wmsdkidl.IWMMetadataEditor.Flush
title: IWMMetadataEditor::Flush (wmsdkidl.h)
description: The Flush method closes the open file, saving any changes.
helpviewer_keywords: ["Flush","Flush method [windows Media Format]","Flush method [windows Media Format]","IWMMetadataEditor interface","IWMMetadataEditor interface [windows Media Format]","Flush method","IWMMetadataEditor.Flush","IWMMetadataEditor::Flush","IWMMetadataEditorFlush","wmformat.iwmmetadataeditor_flush","wmsdkidl/IWMMetadataEditor::Flush"]
old-location: wmformat\iwmmetadataeditor_flush.htm
tech.root: wmformat
ms.assetid: b17992f7-ed93-4f62-bf50-8fb2fd41caee
ms.date: 12/05/2018
ms.keywords: Flush, Flush method [windows Media Format], Flush method [windows Media Format],IWMMetadataEditor interface, IWMMetadataEditor interface [windows Media Format],Flush method, IWMMetadataEditor.Flush, IWMMetadataEditor::Flush, IWMMetadataEditorFlush, wmformat.iwmmetadataeditor_flush, wmsdkidl/IWMMetadataEditor::Flush
f1_keywords:
- wmsdkidl/IWMMetadataEditor.Flush
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
- IWMMetadataEditor.Flush
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMMetadataEditor::Flush


## -description



The <b>Flush</b> method closes the open file, saving any changes.




## -parameters






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




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor">IWMMetadataEditor Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmetadataeditor-close">IWMMetadataEditor::Close</a>
 

 

