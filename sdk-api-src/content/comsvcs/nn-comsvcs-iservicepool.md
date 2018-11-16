---
UID: NN:comsvcs.IServicePool
title: IServicePool
author: windows-sdk-content
description: Used to manage a COM+ object pool.
old-location: cos\iservicepool.htm
tech.root: cossdk
ms.assetid: fb86ffa5-b4cd-48bc-a99e-245e75ddb9c2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IServicePool, IServicePool interface [COM+], IServicePool interface [COM+],described, _cos_IServicePool, comsvcs/IServicePool, cos.iservicepool
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServicePool interface


## -description


Used to manage a COM+ object pool.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServicePool</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IServicePool</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms687813(v=VS.85).aspx">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves an object from the object pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684255(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes an object pool.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686540(v=VS.85).aspx">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down an object pool.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms678840(v=VS.85).aspx">IServicePoolConfig</a>
 

 

