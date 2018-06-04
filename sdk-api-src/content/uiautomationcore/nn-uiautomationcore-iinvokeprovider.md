---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IInvokeProvider interface


## -description


Provides access to controls 
        that initiate or perform a single, unambiguous action and do not maintain state when activated.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInvokeProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInvokeProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInvokeProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9bd2aba1-0751-412c-a6fe-0c10b9baa01e">Invoke</a>
</td>
<td align="left" width="63%">
Sends a request to activate a control and initiate its single, unambiguous action.

</td>
</tr>
</table> 


## -remarks




        Implemented on a Microsoft UI Automation provider that must 
        support the <a href="https://msdn.microsoft.com/6557a03c-fd1f-4e44-8393-fe367d7a17af">Invoke</a> control pattern.
		


        Controls implement <b>IInvokeProvider</b> if the same behavior is not 
        exposed through another  control pattern provider. For example, if 
        the <a href="https://msdn.microsoft.com/9bd2aba1-0751-412c-a6fe-0c10b9baa01e">Invoke</a> method of a control performs the same 
        action as the <a href="https://msdn.microsoft.com/1ac8c1fd-e754-439a-9bcf-92cb0974df91">IExpandCollapseProvider::Expand</a> or <a href="https://msdn.microsoft.com/a4915a1b-9418-4601-9333-f9508d63079a">Collapse</a> 
        method, the control should not also implement <b>IInvokeProvider</b>.
        




## -see-also




<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

