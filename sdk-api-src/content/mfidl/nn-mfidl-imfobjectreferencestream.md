---
UID: NN:mfidl.IMFObjectReferenceStream
title: IMFObjectReferenceStream
author: windows-sdk-content
description: Marshals an interface pointer to and from a stream.Stream objects that support IStream can expose this interface to provide custom marshaling for interface pointers.
old-location: mf\imfobjectreferencestream.htm
tech.root: medfound
ms.assetid: 9d29befd-b0ae-4610-a0b7-17face03c45e
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 9d29befd-b0ae-4610-a0b7-17face03c45e, IMFObjectReferenceStream, IMFObjectReferenceStream interface [Media Foundation], IMFObjectReferenceStream interface [Media Foundation],described, mf.imfobjectreferencestream, mfidl/IMFObjectReferenceStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFObjectReferenceStream interface


## -description



Marshals an interface pointer to and from a stream.

Stream objects that support <b>IStream</b> can expose this interface to provide custom marshaling for interface pointers.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFObjectReferenceStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFObjectReferenceStream</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/fabf7de2-8433-43ba-9ded-001569614054">LoadReference</a>
</td>
<td align="left" width="63%">
Marshals an interface from data stored in the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/776f94c4-d0e9-4fb7-a39c-32c83428bbe3">SaveReference</a>
</td>
<td align="left" width="63%">
Stores the data needed to marshal an interface across a process boundary.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b8bc88e5-19ae-46b3-aa78-a00afee1f481">MFSerializeAttributesToStream</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

