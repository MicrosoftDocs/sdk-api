---
UID: NN:bdaiface.IBDA_ConditionalAccess
title: IBDA_ConditionalAccess (bdaiface.h)
description: The IBDA_ConditionalAccess interface provides conditional access to program content.
helpviewer_keywords: ["IBDA_ConditionalAccess","IBDA_ConditionalAccess interface [Microsoft TV Technologies]","IBDA_ConditionalAccess interface [Microsoft TV Technologies]","described","IBDA_ConditionalAccessInterface","bdaiface/IBDA_ConditionalAccess","mstv.ibda_conditionalaccess"]
old-location: mstv\ibda_conditionalaccess.htm
tech.root: mstv
ms.assetid: 93bd3c38-2591-4d36-b296-5ad939487277
ms.date: 12/05/2018
ms.keywords: IBDA_ConditionalAccess, IBDA_ConditionalAccess interface [Microsoft TV Technologies], IBDA_ConditionalAccess interface [Microsoft TV Technologies],described, IBDA_ConditionalAccessInterface, bdaiface/IBDA_ConditionalAccess, mstv.ibda_conditionalaccess
f1_keywords:
- bdaiface/IBDA_ConditionalAccess
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_ConditionalAccess interface


## -description


The <b>IBDA_ConditionalAccess</b> interface provides conditional access to program content.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/ocur-devices">OCUR Devices</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_ConditionalAccess</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_ConditionalAccess</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_conditionalaccess-addprogram">AddProgram</a>
</td>
<td align="left" width="63%">
Adds a program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_conditionalaccess-get_entitlement">get_Entitlement</a>
</td>
<td align="left" width="63%">
Retrieves the entitlement type for a virtual channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_conditionalaccess-get_smartcardapplications">get_SmartCardApplications</a>
</td>
<td align="left" width="63%">
Retrieves a list of the smart card applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_conditionalaccess-get_smartcardinfo">get_SmartCardInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the smart card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_conditionalaccess-get_smartcardstatus">get_SmartCardStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the smart card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_conditionalaccess-getmoduleui">GetModuleUI</a>
</td>
<td align="left" width="63%">
Retrieves a list of the smart card applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_conditionalaccess-informuiclosed">InformUIClosed</a>
</td>
<td align="left" width="63%">
Informs the device that the user-interface dialog is closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_conditionalaccess-removeprogram">RemoveProgram</a>
</td>
<td align="left" width="63%">
Removes a program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_conditionalaccess-setprogram">SetProgram</a>
</td>
<td align="left" width="63%">
Sets a program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_conditionalaccess-tunebychannel">TuneByChannel</a>
</td>
<td align="left" width="63%">
Tunes to a virtual channel.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof()</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

