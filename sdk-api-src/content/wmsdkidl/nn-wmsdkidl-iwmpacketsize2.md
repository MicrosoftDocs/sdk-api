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
 - IWMPacketSize2
 - wmsdkidl/IWMPacketSize2
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
 - IWMPacketSize2
---

# IWMPacketSize2 interface


## -description

The <b>IWMPacketSize2</b> interface provides methods to set and retrieve the minimum <a href="/windows/desktop/wmformat/wmformat-glossary">packet</a> size for a profile.

An <b>IWMPacketSize2</b> interface can be obtained for either a profile object, a reader object, or a synchronous reader object. You can obtain a pointer to <b>IWMPacketSize2</b> by calling the <b>QueryInterface</b> method of any of the other interfaces in one of the supported objects.

## -inheritance

The <b>IWMPacketSize2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize">IWMPacketSize</a>. <b>IWMPacketSize2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize">IWMPacketSize Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/profile-object">Profile Object</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>
