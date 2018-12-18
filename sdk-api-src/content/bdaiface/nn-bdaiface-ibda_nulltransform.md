---
UID: NN:bdaiface.IBDA_NullTransform
title: IBDA_NullTransform
author: windows-sdk-content
description: The IBDA_NullTransform interface is implemented on all BDA device filters.
old-location: mstv\ibda_nulltransform.htm
tech.root: mstv
ms.assetid: f13350cb-5064-405d-aeb6-25f684d0bdbb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IBDA_NullTransform, IBDA_NullTransform interface [Microsoft TV Technologies], IBDA_NullTransform interface [Microsoft TV Technologies],described, IBDA_NullTransformInterface, bdaiface/IBDA_NullTransform, mstv.ibda_nulltransform
ms.topic: interface
req.header: bdaiface.h
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
 - bdaiface.h
api_name:
 - IBDA_NullTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_NullTransform interface


## -description



The <b>IBDA_NullTransform</b> interface is implemented on all BDA device filters. The Network Provider filter calls these methods to instruct the filter to either pass data through without modifying it, or else to perform its particular transformation on the data.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_NullTransform</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_NullTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_NullTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693419(v=VS.85).aspx">Start</a>
</td>
<td align="left" width="63%">
Restarts the transforms on data flowing through the control node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693420(v=VS.85).aspx">Stop</a>
</td>
<td align="left" width="63%">
Stops the transforms on data flowing through the control node.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_NullTransform)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

