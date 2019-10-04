---
UID: NN:comsvcs.IManagedPooledObj
title: IManagedPooledObj (comsvcs.h)
author: windows-sdk-content
description: Describes how a managed object is used in the COM+ object pool.
old-location: cos\imanagedpooledobj.htm
tech.root: cossdk
ms.assetid: 04853859-5d85-4b88-9e1b-422e3454fd3f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IManagedPooledObj, IManagedPooledObj interface [COM+], IManagedPooledObj interface [COM+],described, _cos_IManagedPooledObj, comsvcs/IManagedPooledObj, cos.imanagedpooledobj
ms.topic: interface
f1_keywords: 
 - "comsvcs/IManagedPooledObj"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IManagedPooledObj interface


## -description


Describes how a managed object is used in the COM+ object pool.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IManagedPooledObj</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IManagedPooledObj</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-imanagedpooledobj-setheld">SetHeld</a>
</td>
<td align="left" width="63%">
Sets whether the managed object should go back into the COM+ object pool.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/com--object-pooling">COM+ Object Pooling</a>



<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-imanagedpoolaction">IManagedPoolAction</a>
 

 

