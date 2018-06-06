---
UID: NN:objidlbase.IMarshalingStream
title: IMarshalingStream
author: windows-sdk-content
description: Provides additional information about the marshaling context to custom-marshaled objects and unmarshalers.
old-location: com\imarshalingstream.htm
old-project: com
ms.assetid: 7C4A3982-3623-4F1F-929C-6D0503700450
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IMarshalingStream, IMarshalingStream interface [COM], IMarshalingStream interface [COM],described, com.imarshalingstream, objidl/IMarshalingStream
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidlbase.h
req.include-header: Objidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidl.h
api_name:
 - IMarshalingStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMarshalingStream interface


## -description


Provides additional information about the marshaling context to custom-marshaled objects and unmarshalers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMarshalingStream</b> interface inherits from <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>. <b>IMarshalingStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMarshalingStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60B401C8-1ACA-412D-B754-997C39454821">GetMarshalingContextAttribute</a>
</td>
<td align="left" width="63%">
Gets information about the marshaling context.

</td>
</tr>
</table> 


## -remarks



Implement <b>IMarshalingStream</b> interface if you have <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> implementations that call the marshaling APIs and provide the correct value of any of the attributes. This is essential only for <b>IStream</b> implementations that are used in hybrid policy processes.




## -see-also




<a href="https://msdn.microsoft.com/7F557290-7162-4B32-880B-9A445A083F91">GLOBALOPT_UNMARSHALING_POLICY_VALUES</a>



<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>
 

 

