---
UID: NN:wmsdkidl.IWMStreamList
title: IWMStreamList (wmsdkidl.h)
description: The IWMStreamList interface is used by mutual exclusion objects and bandwidth sharing objects to maintain lists of streams.
helpviewer_keywords: ["IWMStreamList","IWMStreamList interface [windows Media Format]","IWMStreamList interface [windows Media Format]","described","IWMStreamListInterface","wmformat.iwmstreamlist","wmsdkidl/IWMStreamList"]
old-location: wmformat\iwmstreamlist.htm
tech.root: wmformat
ms.assetid: 076bb0bf-3cf8-48b4-bfca-abbd9c1bf211
ms.date: 12/05/2018
ms.keywords: IWMStreamList, IWMStreamList interface [windows Media Format], IWMStreamList interface [windows Media Format],described, IWMStreamListInterface, wmformat.iwmstreamlist, wmsdkidl/IWMStreamList
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
 - IWMStreamList
 - wmsdkidl/IWMStreamList
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
 - IWMStreamList
---

# IWMStreamList interface


## -description

The <b>IWMStreamList</b> interface is used by mutual exclusion objects and bandwidth sharing objects to maintain lists of streams. The <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion">IWMMutualExclusion</a> and <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing</a> interfaces each inherit from <b>IWMStreamList</b>. These are the only uses of this interface in the SDK. You never need to deal with interface pointers for <b>IWMStreamList</b> directly.

## -inheritance

The <b>IWMStreamList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMStreamList</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/bandwidth-sharing-object">Bandwidth Sharing Object</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/mutual-exclusion-object">Mutual Exclusion Object</a>
