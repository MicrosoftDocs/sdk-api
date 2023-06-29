---
UID: NN:wmsdkidl.IWMMetadataEditor
title: IWMMetadataEditor (wmsdkidl.h)
description: The IWMMetadataEditor interface is used to edit metadata information in ASF file headers. It is obtained by calling the WMCreateEditor function.
helpviewer_keywords: ["IWMMetadataEditor","IWMMetadataEditor interface [windows Media Format]","IWMMetadataEditor interface [windows Media Format]","described","IWMMetadataEditorInterface","wmformat.iwmmetadataeditor","wmsdkidl/IWMMetadataEditor"]
old-location: wmformat\iwmmetadataeditor.htm
tech.root: wmformat
ms.assetid: ad19cd3e-d1ef-4d6c-ac23-29a56e5c1d66
ms.date: 4/26/2023
ms.keywords: IWMMetadataEditor, IWMMetadataEditor interface [windows Media Format], IWMMetadataEditor interface [windows Media Format],described, IWMMetadataEditorInterface, wmformat.iwmmetadataeditor, wmsdkidl/IWMMetadataEditor
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMMetadataEditor
 - wmsdkidl/IWMMetadataEditor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMMetadataEditor
---

# IWMMetadataEditor interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMMetadataEditor</b> interface is used to edit metadata information in ASF file headers. It is obtained by calling the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreateeditor">WMCreateEditor</a> function.

## -inheritance

The <b>IWMMetadataEditor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMMetadataEditor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>
