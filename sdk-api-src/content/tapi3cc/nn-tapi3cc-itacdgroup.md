---
UID: NN:tapi3cc.ITACDGroup
title: ITACDGroup (tapi3cc.h)
description: Automatic Call Distribution (ACD) is a mechanism that queues and distributes calls within a switching system.
old-location: tapi3\itacdgroup.htm
tech.root: Tapi
ms.assetid: 73e23023-5574-4c5a-bdff-cbc7da765a65
ms.date: 12/05/2018
ms.keywords: ITACDGroup, ITACDGroup interface [TAPI 2.2], ITACDGroup interface [TAPI 2.2],described, _tapi3_itacdgroup, tapi3.itacdgroup, tapi3cc/ITACDGroup
f1_keywords:
- tapi3cc/ITACDGroup
dev_langs:
- c++
req.header: tapi3cc.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITACDGroup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITACDGroup interface


## -description


Automatic Call Distribution (ACD) is a mechanism that queues and distributes calls within a switching system. The ACDGroup object reflects an ACD pilot, split, or group. For example, one ACDGroup might handle calls for new accounts while another handles queries on existing accounts. The following methods create the 
<b>ITACDGroup</b> interface:


<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-ienumacdgroup-next">IEnumACDGroup::Next</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-get_acdgroups">ITAgentHandler::get_ACDGroups</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagent-createsession">ITAgent::CreateSession</a>


See 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITACDGroup</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITACDGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITACDGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itacdgroup-enumeratequeues">EnumerateQueues</a>
</td>
<td align="left" width="63%">
Enumerates queues currently on the ACD group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itacdgroup-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Gets the ACD group name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itacdgroup-get_queues">get_Queues</a>
</td>
<td align="left" width="63%">
Creates a collection of queues associated with the current ACD group. Provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
</table> 

