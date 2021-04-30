---
UID: NN:wmsdkidl.IWMDRMWriter
title: IWMDRMWriter (wmsdkidl.h)
description: The IWMDRMWriter interface provides support for applying DRM protection to content in ASF files.
helpviewer_keywords: ["IWMDRMWriter","IWMDRMWriter interface [windows Media Format]","IWMDRMWriter interface [windows Media Format]","described","IWMDRMWriterInterface","wmformat.iwmdrmwriter","wmsdkidl/IWMDRMWriter"]
old-location: wmformat\iwmdrmwriter.htm
tech.root: wmformat
ms.assetid: fd466cf8-b1f8-49aa-a486-8fd347b29178
ms.date: 12/05/2018
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

<p class="CCE_Message">[<b>IWMDRMWriter</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDRMWriter</b> interface provides support for applying DRM protection to content in ASF files. You can use this interface to set various DRM file attributes and run-time properties, and to generate <a href="/windows/desktop/wmformat/wmformat-glossary">DRM</a> keys for encrypting the content and the DRM header, without needing to call functions external to the Windows Media Format SDK. Prior to Windows Media 9 Series, it was necessary to use the Windows Media Rights Manager SDK to apply protection to files. The ability to protect files "on the fly" as you write them enables scenarios such as "Live DRM" in which live streaming content, such as a pay-per-view sports event or concert, can be delivered over the Internet.

An <b>IWMDRMWriter</b> interface exists for every writer object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any interface in a writer object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMWriter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDRMWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/drm-attribute-list">DRM Attribute List</a>



<a href="/windows/desktop/wmformat/drm-properties">DRM Properties</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2">IWMDRMWriter2 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/writer-object">Writer Object</a>
