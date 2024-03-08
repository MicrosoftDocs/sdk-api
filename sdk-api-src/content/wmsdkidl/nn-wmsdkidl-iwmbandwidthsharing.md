---
UID: NN:wmsdkidl.IWMBandwidthSharing
title: IWMBandwidthSharing (wmsdkidl.h)
description: The IWMBandwidthSharing interface contains methods to manage the properties of combined streams.The list of streams that share bandwidth is stored in the bandwidth sharing object.
helpviewer_keywords: ["IWMBandwidthSharing","IWMBandwidthSharing interface [windows Media Format]","IWMBandwidthSharing interface [windows Media Format]","described","IWMBandwidthSharingInterface","wmformat.iwmbandwidthsharing","wmsdkidl/IWMBandwidthSharing"]
old-location: wmformat\iwmbandwidthsharing.htm
tech.root: wmformat
ms.assetid: fd0e48bb-2e5e-4158-9ff1-5b603f219689
ms.date: 4/26/2023
ms.keywords: IWMBandwidthSharing, IWMBandwidthSharing interface [windows Media Format], IWMBandwidthSharing interface [windows Media Format],described, IWMBandwidthSharingInterface, wmformat.iwmbandwidthsharing, wmsdkidl/IWMBandwidthSharing
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
 - IWMBandwidthSharing
 - wmsdkidl/IWMBandwidthSharing
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
 - IWMBandwidthSharing
---

# IWMBandwidthSharing interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMBandwidthSharing</b> interface contains methods to manage the properties of combined streams.

The list of streams that share bandwidth is stored in the bandwidth sharing object. The streams can be manipulated using the methods of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a> interface. <b>IWMBandwidthSharing</b> inherits from <b>IWMStreamList</b>, so the stream list manipulation methods are always exposed through this interface.

The information in a bandwidth sharing object is purely informational. Nothing in the SDK seeks to enforce or check the accuracy of the bandwidth specified. You might want to use bandwidth sharing so that a reading application can make adjustments based on the information contained in the bandwidth sharing object.

An <b>IWMBandwidthSharing</b> interface is exposed for each bandwidth sharing object upon creation. Bandwidth sharing objects are created using the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing">IWMProfile3::CreateNewBandwidthSharing</a> method.

## -inheritance

The <b>IWMBandwidthSharing</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a>. <b>IWMBandwidthSharing</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/bandwidth-sharing-object">Bandwidth Sharing Object</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a>



<a href="/windows/desktop/wmformat/using-bandwidth-sharing">Using Bandwidth Sharing</a>
