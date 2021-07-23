---
UID: NN:wmsdkidl.IWMDRMReader2
title: IWMDRMReader2 (wmsdkidl.h)
description: The IWMDRMReader2 interface provides methods for examining the rights granted by DRM version 10 licenses.An IWMDRMReader2 interface exists for every instance of the reader object.
helpviewer_keywords: ["IWMDRMReader2","IWMDRMReader2 interface [windows Media Format]","IWMDRMReader2 interface [windows Media Format]","described","IWMDRMReader2Interface","wmformat.iwmdrmreader2","wmsdkidl/IWMDRMReader2"]
old-location: wmformat\iwmdrmreader2.htm
tech.root: wmformat
ms.assetid: 9fb7bbeb-d35f-41f7-b39a-2e5a102b5c05
ms.date: 12/05/2018
ms.keywords: IWMDRMReader2, IWMDRMReader2 interface [windows Media Format], IWMDRMReader2 interface [windows Media Format],described, IWMDRMReader2Interface, wmformat.iwmdrmreader2, wmsdkidl/IWMDRMReader2
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IWMDRMReader2
 - wmsdkidl/IWMDRMReader2
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
 - IWMDRMReader2
---

# IWMDRMReader2 interface


## -description

<p class="CCE_Message">[<b>IWMDRMReader2</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDRMReader2</b> interface provides methods for examining the rights granted by DRM version 10 licenses.

An <b>IWMDRMReader2</b> interface exists for every instance of the reader object. You can get a pointer to this method by calling the <b>QueryInterface</b> method of any other interface of the reader object.

## -inheritance

The <b>IWMDRMReader2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader</a>. <b>IWMDRMReader2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader3">IWMDRMReader3 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
