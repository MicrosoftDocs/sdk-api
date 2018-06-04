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

# IATSCComponentType interface


## -description



The <b>IATSCComponentType</b> interface represents a component type for a component in an ATSC broadcast. The <a href="https://msdn.microsoft.com/45c0c3ce-1313-4203-a5e6-af4aed8f0324">ATSCComponentType</a> object exposes this interface. Use this interface to determine if an audio stream is in AC-3 format.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSCComponentType</b> interface inherits from <a href="https://msdn.microsoft.com/10bf35e0-d5bf-41ed-b514-7c1bfaf774a0">IMPEG2ComponentType</a>. <b>IATSCComponentType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSCComponentType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f89f59fd-31bf-48d6-9cb3-92504ba095a9">get_Flags</a>
</td>
<td align="left" width="63%">
Queries whether an audio component is in AC-3 format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e2959a4c-70a8-43a4-8bc5-4bfc965e8085">put_Flags</a>
</td>
<td align="left" width="63%">
Specifies whether an audio component is in AC-3 format.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IATSCComponentType)</code>.




## -see-also




<a href="https://msdn.microsoft.com/10bf35e0-d5bf-41ed-b514-7c1bfaf774a0">IMPEG2ComponentType</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

