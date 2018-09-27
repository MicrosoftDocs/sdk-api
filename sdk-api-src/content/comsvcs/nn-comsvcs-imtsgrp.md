---
UID: NN:comsvcs.IMtsGrp
title: IMtsGrp
author: windows-sdk-content
description: Provides methods for enumerating through running packages.
old-location: cos\imtsgrp.htm
tech.root: cossdk
ms.assetid: 976b4f0a-79cb-4b2d-8d69-225230147c53
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IMtsGrp, IMtsGrp interface [COM+], IMtsGrp interface [COM+],described, _dtc_IMtsGrp_Interface, comsvcs/IMtsGrp, cos.imtsgrp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
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
 - IMtsGrp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMtsGrp interface


## -description


Provides methods for enumerating through running packages.  The events are published to the subscriber using the <a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a> service, a loosely coupled events system that stores event information from different publishers in an event store in the COM+ catalog.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMtsGrp</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IMtsGrp</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IMtsGrp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683575(v=VS.85).aspx">get_Count</a>
</td>
<td align="left" width="63%">
Retrieves the number of running packages in the catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681792(v=VS.85).aspx">Item</a>
</td>
<td align="left" width="63%">
Retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> pointer for the specified package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682788(v=VS.85).aspx">Refresh</a>
</td>
<td align="left" width="63%">
Updates the list of <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> pointers that was populated upon the creation of the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679237(v=VS.85).aspx">COM+ Events</a>



<a href="https://msdn.microsoft.com/en-us/library/ms678896(v=VS.85).aspx">COM+ Instrumentation</a>
 

 

