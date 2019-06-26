---
UID: NN:wmsdkidl.IWMReaderAccelerator
title: IWMReaderAccelerator (wmsdkidl.h)
author: windows-sdk-content
description: The IWMReaderAccelerator interface is implemented on the reader object only when it is in decoding mode. It is called by a player or a player source filter to obtain interfaces from the decoder DMO.
old-location: wmformat\iwmreaderaccelerator.htm
tech.root: wmformat
ms.assetid: cf783b70-4d19-4006-ad0e-e1f883f00b0b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderAccelerator, IWMReaderAccelerator interface [windows Media Format], IWMReaderAccelerator interface [windows Media Format],described, IWMReaderAcceleratorInterface, wmformat.iwmreaderaccelerator, wmsdkidl/IWMReaderAccelerator
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMReaderAccelerator"
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
 - IWMReaderAccelerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAccelerator interface


## -description



The <b>IWMReaderAccelerator</b> interface is implemented on the reader object only when it is in decoding mode. It is called by a player or a player source filter to obtain interfaces from the decoder <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">DMO</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMReaderAccelerator</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMReaderAccelerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMReaderAccelerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderaccelerator-getcodecinterface">GetCodecInterface</a>
</td>
<td align="left" width="63%">
Retrieves pointers to interfaces exposed on the decoder DMO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderaccelerator-notify">Notify</a>
</td>
<td align="left" width="63%">
Called by the source filter to pass in the negotiated media type.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/enabling-directx-video-acceleration">Enabling DirectX Video Acceleration</a>
 

 

