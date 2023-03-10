---
UID: NN:wmsdkidl.IWMPacketSize
title: IWMPacketSize (wmsdkidl.h)
description: The IWMPacketSize interface controls the maximum size of packets in an ASF file.
helpviewer_keywords: ["IWMPacketSize","IWMPacketSize interface [windows Media Format]","IWMPacketSize interface [windows Media Format]","described","IWMPacketSizeInterface","wmformat.iwmpacketsize","wmsdkidl/IWMPacketSize"]
old-location: wmformat\iwmpacketsize.htm
tech.root: wmformat
ms.assetid: 002442fe-46de-49d9-8aff-ad7c9aabc8d1
ms.date: 12/05/2018
ms.keywords: IWMPacketSize, IWMPacketSize interface [windows Media Format], IWMPacketSize interface [windows Media Format],described, IWMPacketSizeInterface, wmformat.iwmpacketsize, wmsdkidl/IWMPacketSize
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
 - IWMPacketSize
 - wmsdkidl/IWMPacketSize
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
 - IWMPacketSize
---

# IWMPacketSize interface


## -description

The <b>IWMPacketSize</b> interface controls the maximum size of <a href="/windows/desktop/wmformat/wmformat-glossary">packets</a> in an ASF file. Its methods are used to control the size of <a href="/windows/desktop/wmformat/wmformat-glossary">UDP</a> datagrams when the content, live or on-demand, is streamed across a network.

An <b>IWMPacketSize</b> interface can be obtained for either a profile object, a reader object, or a synchronous reader object. You can obtain a pointer to <b>IWMPacketSize</b> by calling the <b>QueryInterface</b> method of any of the other interfaces in one of the supported objects.

## -inheritance

The <b>IWMPacketSize</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPacketSize</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>
