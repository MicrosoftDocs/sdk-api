---
UID: NN:wmsdkidl.IWMPacketSize2
title: IWMPacketSize2 (wmsdkidl.h)
description: The IWMPacketSize2 interface provides methods to set and retrieve the minimum packet size for a profile.An IWMPacketSize2 interface can be obtained for either a profile object, a reader object, or a synchronous reader object.
helpviewer_keywords: ["IWMPacketSize2","IWMPacketSize2 interface [windows Media Format]","IWMPacketSize2 interface [windows Media Format]","described","IWMPacketSize2Interface","wmformat.iwmpacketsize2","wmsdkidl/IWMPacketSize2"]
old-location: wmformat\iwmpacketsize2.htm
tech.root: wmformat
ms.assetid: 4af4c088-9fc3-46a9-8451-518b11bc94e3
ms.date: 12/05/2018
ms.keywords: IWMPacketSize2, IWMPacketSize2 interface [windows Media Format], IWMPacketSize2 interface [windows Media Format],described, IWMPacketSize2Interface, wmformat.iwmpacketsize2, wmsdkidl/IWMPacketSize2
f1_keywords:
- wmsdkidl/IWMPacketSize2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsdkidl.h
api_name:
- IWMPacketSize2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPacketSize2 interface


## -description



The <b>IWMPacketSize2</b> interface provides methods to set and retrieve the minimum <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">packet</a> size for a profile.

An <b>IWMPacketSize2</b> interface can be obtained for either a profile object, a reader object, or a synchronous reader object. You can obtain a pointer to <b>IWMPacketSize2</b> by calling the <b>QueryInterface</b> method of any of the other interfaces in one of the supported objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPacketSize2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize">IWMPacketSize</a>. <b>IWMPacketSize2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPacketSize2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpacketsize2-getminpacketsize">GetMinPacketSize</a>
</td>
<td align="left" width="63%">
Retrieves the minimum packet size for files created with the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpacketsize2-setminpacketsize">SetMinPacketSize</a>
</td>
<td align="left" width="63%">
Sets the minimum packet size for files created with the profile.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize">IWMPacketSize Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/profile-object">Profile Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>
 

 

