---
UID: NN:comsvcs.IManagedPooledObj
title: IManagedPooledObj
author: windows-sdk-content
description: Describes how a managed object is used in the COM+ object pool.
old-location: cos\imanagedpooledobj.htm
tech.root: cossdk
ms.assetid: 04853859-5d85-4b88-9e1b-422e3454fd3f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IManagedPooledObj, IManagedPooledObj interface [COM+], IManagedPooledObj interface [COM+],described, _cos_IManagedPooledObj, comsvcs/IManagedPooledObj, cos.imanagedpooledobj
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ComSvcs.h
api_name:
 - IManagedPooledObj
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IManagedPooledObj interface


## -description


Describes how a managed object is used in the COM+ object pool.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IManagedPooledObj</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IManagedPooledObj</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IManagedPooledObj</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36e7f210-0532-424f-b958-a7a1be904b3c">SetHeld</a>
</td>
<td align="left" width="63%">
Sets whether the managed object should go back into the COM+ object pool.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/954cf9ee-e76c-4faf-99aa-3648a7bb8a59">COM+ Object Pooling</a>



<a href="https://msdn.microsoft.com/6c29bbe0-840f-4eaf-97ad-40b0f89cadfd">IManagedPoolAction</a>
 

 

