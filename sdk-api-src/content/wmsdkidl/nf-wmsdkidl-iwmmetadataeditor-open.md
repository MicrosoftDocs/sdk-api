---
UID: NF:wmsdkidl.IWMMetadataEditor.Open
title: IWMMetadataEditor::Open (wmsdkidl.h)
description: The Open method opens an ASF file.
helpviewer_keywords: ["IWMMetadataEditor interface [windows Media Format]","Open method","IWMMetadataEditor.Open","IWMMetadataEditor::Open","IWMMetadataEditorOpen","Open","Open method [windows Media Format]","Open method [windows Media Format]","IWMMetadataEditor interface","wmformat.iwmmetadataeditor_open","wmsdkidl/IWMMetadataEditor::Open"]
old-location: wmformat\iwmmetadataeditor_open.htm
tech.root: wmformat
ms.assetid: 01dd09ff-35d2-4e00-9eab-5110a426449f
ms.date: 4/26/2023
ms.keywords: IWMMetadataEditor interface [windows Media Format],Open method, IWMMetadataEditor.Open, IWMMetadataEditor::Open, IWMMetadataEditorOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMMetadataEditor interface, wmformat.iwmmetadataeditor_open, wmsdkidl/IWMMetadataEditor::Open
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
 - IWMMetadataEditor::Open
 - wmsdkidl/IWMMetadataEditor::Open
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
 - IWMMetadataEditor.Open
---

# IWMMetadataEditor::Open


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Open</b> method opens an ASF file.

## -parameters

### -param pwszFilename [in]

Pointer to a wide-character <b>null</b>-terminated string containing the file name.

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
<dt><b>NS_E_FILE_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The method failed to open the specified file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszFilename</i> parameter is <b>NULL</b>.

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



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmetadataeditor2-openex">IWMMetadataEditor2::OpenEx</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmetadataeditor-close">IWMMetadataEditor::Close</a>