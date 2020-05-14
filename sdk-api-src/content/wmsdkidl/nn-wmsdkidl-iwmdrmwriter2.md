---
UID: NN:wmsdkidl.IWMDRMWriter2
title: IWMDRMWriter2 (wmsdkidl.h)
description: The IWMDRMWriter2 interface provides a method that enables you to write content encrypted with Windows Media DRM 10 for Network Devices.An IWMDRMWriter2 interface exists for every writer object.helpviewer_keywords: ["IWMDRMWriter2","IWMDRMWriter2 interface [windows Media Format]","IWMDRMWriter2 interface [windows Media Format]","described","IWMDRMWriter2Interface","wmformat.iwmdrmwriter2","wmsdkidl/IWMDRMWriter2"]
old-location: wmformat\iwmdrmwriter2.htm
tech.root: wmformat
ms.assetid: 8511b464-1f47-4184-9cb7-9aca0cb6660f
ms.date: 12/05/2018
ms.keywords: IWMDRMWriter2, IWMDRMWriter2 interface [windows Media Format], IWMDRMWriter2 interface [windows Media Format],described, IWMDRMWriter2Interface, wmformat.iwmdrmwriter2, wmsdkidl/IWMDRMWriter2
f1_keywords:
- wmsdkidl/IWMDRMWriter2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsdkidl.h
api_name:
- IWMDRMWriter2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDRMWriter2 interface


## -description


<p class="CCE_Message">[<b>IWMDRMWriter2</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDRMWriter2</b> interface provides a method that enables you to write content encrypted with Windows Media DRM 10 for Network Devices.

An <b>IWMDRMWriter2</b> interface exists for every writer object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any interface of a writer object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMWriter2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter">IWMDRMWriter</a>. <b>IWMDRMWriter2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDRMWriter2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmwriter2-setwmdrmnetencryption">SetWMDRMNetEncryption</a>
</td>
<td align="left" width="63%">
Configures the writer to receive input samples encoded for Windows Media DRM 10 for Network Devices delivery.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter">IWMDRMWriter Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/writer-object">Writer Object</a>
 

 

