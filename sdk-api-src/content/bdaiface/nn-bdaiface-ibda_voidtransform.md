---
UID: NN:bdaiface.IBDA_VoidTransform
title: IBDA_VoidTransform
author: windows-sdk-content
description: The IBDA_VoidTransform interface is implemented on a BDA device filter. It is used by the Network Provider to inactivate a portion of a filter graph without stopping the graph.
old-location: mstv\ibda_voidtransform.htm
tech.root: MSTV
ms.assetid: 120638ce-b35f-450e-9675-708495ddd082
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IBDA_VoidTransform, IBDA_VoidTransform interface [Microsoft TV Technologies], IBDA_VoidTransform interface [Microsoft TV Technologies],described, IBDA_VoidTransformInterface, bdaiface/IBDA_VoidTransform, mstv.ibda_voidtransform
ms.prod: windows
ms.technology: windows-sdk
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
 - IBDA_VoidTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBDA_VoidTransform interface


## -description



The <b>IBDA_VoidTransform</b> interface is implemented on a BDA device filter. It is used by the Network Provider to inactivate a portion of a filter graph without stopping the graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_VoidTransform</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IBDA_VoidTransform</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IBDA_VoidTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693462(v=VS.85).aspx">Start</a>
</td>
<td align="left" width="63%">
Restarts data flow through a control node.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693463(v=VS.85).aspx">Stop</a>
</td>
<td align="left" width="63%">
Stops data flow through a control node.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_VoidTransform)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd693008(v=VS.85).aspx">BDA Interfaces</a>
 

 

