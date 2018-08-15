---
UID: NN:comsvcs.IManagedPoolAction
title: IManagedPoolAction
author: windows-sdk-content
description: Enables an object to be notified before it is released from a COM+ object pool.
old-location: cos\imanagedpoolaction.htm
old-project: cossdk
ms.assetid: 6c29bbe0-840f-4eaf-97ad-40b0f89cadfd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IManagedPoolAction, IManagedPoolAction interface [COM+], IManagedPoolAction interface [COM+],described, _cos_IManagedPoolAction, comsvcs/IManagedPoolAction, cos.imanagedpoolaction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IManagedPoolAction
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IManagedPoolAction interface


## -description


Enables an object to be notified before it is released from a COM+ object pool.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IManagedPoolAction</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IManagedPoolAction</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IManagedPoolAction</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6685da39-17bb-4c4e-b47a-888511f605ad">LastRelease</a>
</td>
<td align="left" width="63%">
Called when a COM+ object pool drops the last reference to the object that implements it.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/954cf9ee-e76c-4faf-99aa-3648a7bb8a59">COM+ Object Pooling</a>



<a href="https://msdn.microsoft.com/04853859-5d85-4b88-9e1b-422e3454fd3f">IManagedPooledObj</a>
 

 

