---
UID: NN:wmsdkidl.IWMDRMEditor
title: IWMDRMEditor (wmsdkidl.h)
description: The IWMDRMEditor interface is exposed on the metadata editor object.
helpviewer_keywords: ["IWMDRMEditor","IWMDRMEditor interface [windows Media Format]","IWMDRMEditor interface [windows Media Format]","described","IWMDRMEditorInterface","wmformat.iwmdrmeditor","wmsdkidl/IWMDRMEditor"]
old-location: wmformat\iwmdrmeditor.htm
tech.root: wmformat
ms.assetid: a404d30d-0b42-44c9-93e6-3eb9ef9e40fc
ms.date: 4/26/2023
ms.keywords: IWMDRMEditor, IWMDRMEditor interface [windows Media Format], IWMDRMEditor interface [windows Media Format],described, IWMDRMEditorInterface, wmformat.iwmdrmeditor, wmsdkidl/IWMDRMEditor
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDRMEditor
 - wmsdkidl/IWMDRMEditor
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
 - IWMDRMEditor
---

# IWMDRMEditor interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>IWMDRMEditor</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDRMEditor</b> interface is exposed on the metadata editor object. It can be obtained by calling <b>QueryInterface</b> from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor">IWMMetadataEditor</a>. The <b>IWMDRMEditor</b> interface enables applications to examine the <a href="/windows/desktop/wmformat/wmformat-glossary">DRM</a> attributes of an ASF file, for example to query the number of times a file is allowed to be played, without having the wmstubdrm.lib static library. The <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader</a> interface contains a similar method, but the application must be linked to a valid wmstubdrm.lib library in order to use that interface.

## -inheritance

The <b>IWMDRMEditor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDRMEditor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty">IWMDRMReader::GetDRMProperty</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/metadata-editor-object">Metadata Editor Object</a>



<a href="/windows/desktop/wmformat/viewing-attributes-of-protected-files">Viewing Attributes of Protected Files</a>
