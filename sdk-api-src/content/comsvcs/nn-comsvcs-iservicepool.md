---
UID: NN:comsvcs.IServicePool
title: IServicePool (comsvcs.h)
author: windows-sdk-content
description: Used to manage a COM+ object pool.
old-location: cos\iservicepool.htm
tech.root: cossdk
ms.assetid: fb86ffa5-b4cd-48bc-a99e-245e75ddb9c2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IServicePool, IServicePool interface [COM+], IServicePool interface [COM+],described, _cos_IServicePool, comsvcs/IServicePool, cos.iservicepool
ms.topic: interface
f1_keywords: 
 - "comsvcs/IServicePool"
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional with SP4, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
 - IServicePool
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServicePool interface


## -description


Used to manage a COM+ object pool.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServicePool</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServicePool</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServicePool</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepool-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves an object from the object pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepool-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object pool.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nf-comsvcs-iservicepool-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down an object pool.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-iservicepoolconfig">IServicePoolConfig</a>
 

 

