---
UID: NN:bdaiface.IBDA_ConditionalAccess
title: IBDA_ConditionalAccess (bdaiface.h)
author: windows-sdk-content
description: The IBDA_ConditionalAccess interface provides conditional access to program content.
old-location: mstv\ibda_conditionalaccess.htm
tech.root: mstv
ms.assetid: 93bd3c38-2591-4d36-b296-5ad939487277
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IBDA_ConditionalAccess, IBDA_ConditionalAccess interface [Microsoft TV Technologies], IBDA_ConditionalAccess interface [Microsoft TV Technologies],described, IBDA_ConditionalAccessInterface, bdaiface/IBDA_ConditionalAccess, mstv.ibda_conditionalaccess
ms.topic: interface
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - Bdaiface.h
api_name:
 - IBDA_ConditionalAccess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_ConditionalAccess interface


## -description


The <b>IBDA_ConditionalAccess</b> interface provides conditional access to program content.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://msdn.microsoft.com/7b641b94-9854-4ca8-8362-a9e1e49bbdd2">OCUR Devices</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_ConditionalAccess</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_ConditionalAccess</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_ConditionalAccess</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693268(v=VS.85).aspx">AddProgram</a>
</td>
<td align="left" width="63%">
Adds a program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693270(v=VS.85).aspx">get_Entitlement</a>
</td>
<td align="left" width="63%">
Retrieves the entitlement type for a virtual channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693271(v=VS.85).aspx">get_SmartCardApplications</a>
</td>
<td align="left" width="63%">
Retrieves a list of the smart card applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693272(v=VS.85).aspx">get_SmartCardInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the smart card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693273(v=VS.85).aspx">get_SmartCardStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the smart card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693269(v=VS.85).aspx">GetModuleUI</a>
</td>
<td align="left" width="63%">
Retrieves a list of the smart card applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693274(v=VS.85).aspx">InformUIClosed</a>
</td>
<td align="left" width="63%">
Informs the device that the user-interface dialog is closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693275(v=VS.85).aspx">RemoveProgram</a>
</td>
<td align="left" width="63%">
Removes a program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693276(v=VS.85).aspx">SetProgram</a>
</td>
<td align="left" width="63%">
Sets a program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd693277(v=VS.85).aspx">TuneByChannel</a>
</td>
<td align="left" width="63%">
Tunes to a virtual channel.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof()</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

