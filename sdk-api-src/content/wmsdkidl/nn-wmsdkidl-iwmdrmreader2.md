---
UID: NN:wmsdkidl.IWMDRMReader2
title: IWMDRMReader2 (wmsdkidl.h)
description: The IWMDRMReader2 interface provides methods for examining the rights granted by DRM version 10 licenses.An IWMDRMReader2 interface exists for every instance of the reader object.
helpviewer_keywords: ["IWMDRMReader2","IWMDRMReader2 interface [windows Media Format]","IWMDRMReader2 interface [windows Media Format]","described","IWMDRMReader2Interface","wmformat.iwmdrmreader2","wmsdkidl/IWMDRMReader2"]
old-location: wmformat\iwmdrmreader2.htm
tech.root: wmformat
ms.assetid: 9fb7bbeb-d35f-41f7-b39a-2e5a102b5c05
ms.date: 4/26/2023
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

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>IWMDRMReader2</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDRMReader2</b> interface provides methods for examining the rights granted by DRM version 10 licenses.

An <b>IWMDRMReader2</b> interface exists for every instance of the reader object. You can get a pointer to this method by calling the <b>QueryInterface</b> method of any other interface of the reader object.

## -inheritance

The <b>IWMDRMReader2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader</a>. <b>IWMDRMReader2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader">IWMDRMReader Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader3">IWMDRMReader3 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
