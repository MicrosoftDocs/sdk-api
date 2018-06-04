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

# IMPEG2TuneRequestFactory interface


## -description



The <b>IMPEG2TuneRequestFactory</b> interface creates a tune request for a basic MPEG-2 transport stream containing the minimal tables. To obtain this interface, call <b>CoCreateInstance</b> with the class identifier CLSID_MPEG2TuneRequestFactory.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMPEG2TuneRequestFactory</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IMPEG2TuneRequestFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMPEG2TuneRequestFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41e299d6-492e-40b4-955f-603b18da0c02">CreateTuneRequest</a>
</td>
<td align="left" width="63%">
Creates the minimal MPEG-2 tune request for a specified tuning space

</td>
</tr>
</table> 


## -remarks




        To create a full tune request, use the <a href="https://msdn.microsoft.com/b22ccd86-b8d7-4dd7-af4b-b99c9fea0de5">CreateTuneRequest</a> method provided by one of the tuning space objects.
      

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMPEG2TuneRequestFactory)</code>.




## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

