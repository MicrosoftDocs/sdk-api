---
UID: NN:wmsdkidl.IWMDRMWriter3
title: IWMDRMWriter3 (wmsdkidl.h)
description: The IWMDRMWriter3 interface enables writing of encrypted stream samples for importing protected content.An IWMDRMWriter3 interface exists for every writer object when linking to WMStubDRM.lib.
helpviewer_keywords: ["IWMDRMWriter3","IWMDRMWriter3 interface [windows Media Format]","IWMDRMWriter3 interface [windows Media Format]","described","IWMDRMWriter3Interface","wmformat.iwmdrmwriter3","wmsdkidl/IWMDRMWriter3"]
old-location: wmformat\iwmdrmwriter3.htm
tech.root: wmformat
ms.assetid: b300b97b-e558-4c33-a84a-e92c28a3a606
ms.date: 12/05/2018
ms.keywords: IWMDRMWriter3, IWMDRMWriter3 interface [windows Media Format], IWMDRMWriter3 interface [windows Media Format],described, IWMDRMWriter3Interface, wmformat.iwmdrmwriter3, wmsdkidl/IWMDRMWriter3
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
 - IWMDRMWriter3
 - wmsdkidl/IWMDRMWriter3
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
 - IWMDRMWriter3
---

# IWMDRMWriter3 interface


## -description

<p class="CCE_Message">[<b>IWMDRMWriter3</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDRMWriter3</b> interface enables writing of encrypted stream samples for importing protected content.

An <b>IWMDRMWriter3</b> interface exists for every writer object when linking to WMStubDRM.lib. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any interface of a writer object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMWriter3</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter">IWMDRMWriter</a> and <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2">IWMDRMWriter2</a>. <b>IWMDRMWriter3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter">IWMDRMWriter</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2">IWMDRMWriter2</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
