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

# IControlInterface interface


## -description



The <b>IControlInterface</b> interface represents a control interface on a part (connector or subunit) in a <a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">device topology</a>. The client obtains a reference to a part's <b>IControlInterface</b> interface by calling the <a href="https://msdn.microsoft.com/802f3c19-5a71-41b0-922a-f216fd60495c">IPart::GetControlInterface</a> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IControlInterface</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IControlInterface</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IControlInterface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6d46f37-6b9a-4d20-8a97-9fb5284dbc42">GetIID</a>
</td>
<td align="left" width="63%">
Gets the interface ID of the function-specific control interface of the part.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/591e96ba-aaf1-42ba-9526-f839c30947d3">GetName</a>
</td>
<td align="left" width="63%">
Gets the friendly name for the audio function that the control interface encapsulates.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/051311ef-dd29-4014-bb9c-4cdccf7ce7de">DeviceTopology API</a>



<a href="https://msdn.microsoft.com/802f3c19-5a71-41b0-922a-f216fd60495c">IPart::GetControlInterface</a>
 

 

