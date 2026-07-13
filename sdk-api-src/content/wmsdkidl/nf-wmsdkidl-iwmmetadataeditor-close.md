---
UID: NF:wmsdkidl.IWMMetadataEditor.Close
title: IWMMetadataEditor::Close (wmsdkidl.h)
description: The Close method closes the open file without saving any changes.
helpviewer_keywords: ["Close","Close method [windows Media Format]","Close method [windows Media Format]","IWMMetadataEditor interface","IWMMetadataEditor interface [windows Media Format]","Close method","IWMMetadataEditor.Close","IWMMetadataEditor::Close","IWMMetadataEditorClose","wmformat.iwmmetadataeditor_close","wmsdkidl/IWMMetadataEditor::Close"]
old-location: wmformat\iwmmetadataeditor_close.htm
tech.root: wmformat
ms.assetid: 7c10d0ea-8a19-4374-94f2-e12d7c1ba553
ms.date: 4/26/2023
ms.keywords: Close, Close method [windows Media Format], Close method [windows Media Format],IWMMetadataEditor interface, IWMMetadataEditor interface [windows Media Format],Close method, IWMMetadataEditor.Close, IWMMetadataEditor::Close, IWMMetadataEditorClose, wmformat.iwmmetadataeditor_close, wmsdkidl/IWMMetadataEditor::Close
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
 - IWMMetadataEditor::Close
 - wmsdkidl/IWMMetadataEditor::Close
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
 - IWMMetadataEditor.Close
---

# IWMMetadataEditor::Close


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Close</b> method closes the open file without saving any changes.



## -returns

This method always returns S_OK.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor">IWMMetadataEditor Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmetadataeditor-flush">IWMMetadataEditor::Flush</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmetadataeditor-open">IWMMetadataEditor::Open</a>
