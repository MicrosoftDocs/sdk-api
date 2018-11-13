---
UID: NN:tapi3.ITACDGroup
title: ITACDGroup
author: windows-sdk-content
description: Automatic Call Distribution (ACD) is a mechanism that queues and distributes calls within a switching system.
old-location: tapi3\itacdgroup.htm
tech.root: tapi
ms.assetid: 73e23023-5574-4c5a-bdff-cbc7da765a65
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITACDGroup, ITACDGroup interface [TAPI 2.2], ITACDGroup interface [TAPI 2.2],described, _tapi3_itacdgroup, tapi3.itacdgroup, tapi3cc/ITACDGroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: tapi3.h
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITACDGroup interface


## -description


Automatic Call Distribution (ACD) is a mechanism that queues and distributes calls within a switching system. The ACDGroup object reflects an ACD pilot, split, or group. For example, one ACDGroup might handle calls for new accounts while another handles queries on existing accounts. The following methods create the 
<b>ITACDGroup</b> interface:


<a href="https://msdn.microsoft.com/20cad3aa-2c8c-4ef8-bb3a-b7662b125475">IEnumACDGroup::Next</a>



<a href="https://msdn.microsoft.com/72dcc4c8-fac6-4635-995e-18a5693da99b">ITAgentHandler::get_ACDGroups</a>



<a href="https://msdn.microsoft.com/68cc2ffe-3c63-4723-8652-0e28da2b17b6">ITAgent::CreateSession</a>


See 
<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a> for additional information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITACDGroup</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITACDGroup</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1d9e0dcf-ce43-494f-8adc-845d2856bdd1">EnumerateQueues</a>
</td>
<td align="left" width="63%">
Enumerates queues currently on the ACD group.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/93e61a42-3e60-4d52-bb19-68842f6947da">get_Name</a>
</td>
<td align="left" width="63%">
Gets the ACD group name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f285fea5-4c08-4d30-8378-0b0aeeea8226">get_Queues</a>
</td>
<td align="left" width="63%">
Creates a collection of queues associated with the current ACD group. Provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
</table> 

