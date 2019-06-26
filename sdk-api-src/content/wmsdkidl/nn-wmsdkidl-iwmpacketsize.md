---
UID: NN:wmsdkidl.IWMPacketSize
title: IWMPacketSize (wmsdkidl.h)
author: windows-sdk-content
description: The IWMPacketSize interface controls the maximum size of packets in an ASF file.
old-location: wmformat\iwmpacketsize.htm
tech.root: wmformat
ms.assetid: 002442fe-46de-49d9-8aff-ad7c9aabc8d1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPacketSize, IWMPacketSize interface [windows Media Format], IWMPacketSize interface [windows Media Format],described, IWMPacketSizeInterface, wmformat.iwmpacketsize, wmsdkidl/IWMPacketSize
ms.topic: interface
f1_keywords: 
 - "wmsdkidl/IWMPacketSize"
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
 - IWMPacketSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPacketSize interface


## -description



The <b>IWMPacketSize</b> interface controls the maximum size of <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">packets</a> in an ASF file. Its methods are used to control the size of <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">UDP</a> datagrams when the content, live or on-demand, is streamed across a network.

An <b>IWMPacketSize</b> interface can be obtained for either a profile object, a reader object, or a synchronous reader object. You can obtain a pointer to <b>IWMPacketSize</b> by calling the <b>QueryInterface</b> method of any of the other interfaces in one of the supported objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPacketSize</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPacketSize</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPacketSize</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpacketsize-getmaxpacketsize">GetMaxPacketSize</a>
</td>
<td align="left" width="63%">
Retrieves the maximum size of a packet in an ASF file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmpacketsize-setmaxpacketsize">SetMaxPacketSize</a>
</td>
<td align="left" width="63%">
Specifies the maximum size of a packet in an ASF file.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>
 

 

