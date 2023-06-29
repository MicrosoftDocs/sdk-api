---
UID: NN:wmsdkidl.IWMMetadataEditor2
title: IWMMetadataEditor2 (wmsdkidl.h)
description: The IWMMetadataEditor2 interface provides an improved method for opening files for metadata operations.This interface is implemented as part of the metadata editor object.
helpviewer_keywords: ["IWMMetadataEditor2","IWMMetadataEditor2 interface [windows Media Format]","IWMMetadataEditor2 interface [windows Media Format]","described","IWMMetadataEditor2Interface","wmformat.iwmmetadataeditor2","wmsdkidl/IWMMetadataEditor2"]
old-location: wmformat\iwmmetadataeditor2.htm
tech.root: wmformat
ms.assetid: e991ac8e-35af-484f-8c60-dc6a7d402120
ms.date: 4/26/2023
ms.keywords: IWMMetadataEditor2, IWMMetadataEditor2 interface [windows Media Format], IWMMetadataEditor2 interface [windows Media Format],described, IWMMetadataEditor2Interface, wmformat.iwmmetadataeditor2, wmsdkidl/IWMMetadataEditor2
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
 - IWMMetadataEditor2
 - wmsdkidl/IWMMetadataEditor2
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
 - IWMMetadataEditor2
---

# IWMMetadataEditor2 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMMetadataEditor2</b> interface provides an improved method for opening files for metadata operations.

This interface is implemented as part of the metadata editor object. To obtain a pointer to <b>IWMMetadataEditor2</b>, call the <b>QueryInterface</b> method of any other interface in an existing metadata editor object.

## -inheritance

The <b>IWMMetadataEditor2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor">IWMMetadataEditor</a>. <b>IWMMetadataEditor2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor">IWMMetadataEditor Interface</a>



<a href="/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>
