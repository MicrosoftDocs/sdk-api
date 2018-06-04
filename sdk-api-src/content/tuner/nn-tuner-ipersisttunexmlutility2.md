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

# IPersistTuneXmlUtility2 interface


## -description



      Defines utility methods for serializing tuning requests (objects that implement the <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface) to XML tuning request strings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistTuneXmlUtility2</b> interface inherits from <a href="https://msdn.microsoft.com/aa03015f-094f-499f-99fb-2e15ead74f15">IPersistTuneXmlUtility</a>. <b>IPersistTuneXmlUtility2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistTuneXmlUtility2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/463ddd94-5eb1-4553-a31d-0a06326eceec">Serialize</a>
</td>
<td align="left" width="63%">
Constructs and returns an object that serializes a tuning request to an XML node.
    
          

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IPersistTuneXmlUtility2)</code>.




## -see-also




<a href="https://msdn.microsoft.com/aa03015f-094f-499f-99fb-2e15ead74f15">IPersistTuneXmlUtility</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

