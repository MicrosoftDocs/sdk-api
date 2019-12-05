---
UID: NN:mfidl.IMFObjectReferenceStream
title: IMFObjectReferenceStream (mfidl.h)
description: Marshals an interface pointer to and from a stream.Stream objects that support IStream can expose this interface to provide custom marshaling for interface pointers.
old-location: mf\imfobjectreferencestream.htm
tech.root: medfound
ms.assetid: 9d29befd-b0ae-4610-a0b7-17face03c45e
ms.date: 12/05/2018
ms.keywords: 9d29befd-b0ae-4610-a0b7-17face03c45e, IMFObjectReferenceStream, IMFObjectReferenceStream interface [Media Foundation], IMFObjectReferenceStream interface [Media Foundation],described, mf.imfobjectreferencestream, mfidl/IMFObjectReferenceStream
ms.topic: interface
f1_keywords:
- mfidl/IMFObjectReferenceStream
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFObjectReferenceStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFObjectReferenceStream interface


## -description



Marshals an interface pointer to and from a stream.

Stream objects that support <b>IStream</b> can expose this interface to provide custom marshaling for interface pointers.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFObjectReferenceStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFObjectReferenceStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFObjectReferenceStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfobjectreferencestream-loadreference">LoadReference</a>
</td>
<td align="left" width="63%">
Marshals an interface from data stored in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfobjectreferencestream-savereference">SaveReference</a>
</td>
<td align="left" width="63%">
Stores the data needed to marshal an interface across a process boundary.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream">MFSerializeAttributesToStream</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

