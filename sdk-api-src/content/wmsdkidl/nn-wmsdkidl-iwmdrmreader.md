---
UID: NN:wmsdkidl.IWMDRMReader
title: IWMDRMReader (wmsdkidl.h)
description: The IWMDRMReader interface provides methods to configure the DRM component and to manage DRM license acquisition and individualization of client applications.
helpviewer_keywords: ["IWMDRMReader","IWMDRMReader interface [windows Media Format]","IWMDRMReader interface [windows Media Format]","described","IWMDRMReaderInterface","wmformat.iwmdrmreader","wmsdkidl/IWMDRMReader"]
old-location: wmformat\iwmdrmreader.htm
tech.root: wmformat
ms.assetid: bf4ff0f3-1f78-43c4-be4d-c74209176e58
ms.date: 12/05/2018
ms.keywords: IWMDRMReader, IWMDRMReader interface [windows Media Format], IWMDRMReader interface [windows Media Format],described, IWMDRMReaderInterface, wmformat.iwmdrmreader, wmsdkidl/IWMDRMReader
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
 - IWMDRMReader
 - wmsdkidl/IWMDRMReader
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
 - IWMDRMReader
---

# IWMDRMReader interface


## -description

<p class="CCE_Message">[<b>IWMDRMReader</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDRMReader</b> interface provides methods to configure the DRM component and to manage <a href="/windows/desktop/wmformat/wmformat-glossary">DRM</a> license acquisition and individualization of client applications. It is used only for content protected using DRM version 7, not the earlier DRM version 1.

This interface can be obtained from a reader object.

## -inheritance

The <b>IWMDRMReader</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDRMReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/drm-attribute-list">DRM Attribute List</a>



<a href="/windows/desktop/wmformat/drm-properties">DRM Properties</a>



<a href="/windows/desktop/wmformat/digital-rights-management-features">Digital Rights Management Features</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2">IWMDRMReader2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader3">IWMDRMReader3 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader">IWMReader Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
