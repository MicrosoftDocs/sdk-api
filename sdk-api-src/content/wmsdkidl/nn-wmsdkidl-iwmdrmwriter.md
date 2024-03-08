---
UID: NN:wmsdkidl.IWMDRMWriter
title: IWMDRMWriter (wmsdkidl.h)
description: The IWMDRMWriter interface provides support for applying DRM protection to content in ASF files.
helpviewer_keywords: ["IWMDRMWriter","IWMDRMWriter interface [windows Media Format]","IWMDRMWriter interface [windows Media Format]","described","IWMDRMWriterInterface","wmformat.iwmdrmwriter","wmsdkidl/IWMDRMWriter"]
old-location: wmformat\iwmdrmwriter.htm
tech.root: wmformat
ms.assetid: fd466cf8-b1f8-49aa-a486-8fd347b29178
ms.date: 4/26/2023
ms.keywords: IWMDRMWriter, IWMDRMWriter interface [windows Media Format], IWMDRMWriter interface [windows Media Format],described, IWMDRMWriterInterface, wmformat.iwmdrmwriter, wmsdkidl/IWMDRMWriter
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
 - IWMDRMWriter
 - wmsdkidl/IWMDRMWriter
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
 - IWMDRMWriter
---

# IWMDRMWriter interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>IWMDRMWriter</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDRMWriter</b> interface provides support for applying DRM protection to content in ASF files. You can use this interface to set various DRM file attributes and run-time properties, and to generate <a href="/windows/desktop/wmformat/wmformat-glossary">DRM</a> keys for encrypting the content and the DRM header, without needing to call functions external to the Windows Media Format SDK. Prior to Windows Media 9 Series, it was necessary to use the Windows Media Rights Manager SDK to apply protection to files. The ability to protect files "on the fly" as you write them enables scenarios such as "Live DRM" in which live streaming content, such as a pay-per-view sports event or concert, can be delivered over the Internet.

An <b>IWMDRMWriter</b> interface exists for every writer object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any interface in a writer object.

## -inheritance

The <b>IWMDRMWriter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDRMWriter</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/drm-attribute-list">DRM Attribute List</a>



<a href="/windows/desktop/wmformat/drm-properties">DRM Properties</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2">IWMDRMWriter2 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>
