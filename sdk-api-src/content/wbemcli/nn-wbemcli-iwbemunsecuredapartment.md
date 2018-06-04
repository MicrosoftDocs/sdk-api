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

# IWbemUnsecuredApartment interface


## -description


The <b>IWbemUnsecuredApartment</b> interface 
   allows client applications to determine whether Unsecapp.exe performs access 
   checks on asynchronous callbacks. Unsecapp.exe supports both 
   <a href="https://msdn.microsoft.com/6293d8e3-cc5b-4401-8fdc-86f5d03720ea">IUnsecuredApartment</a> and 
   <b>IWbemUnsecuredApartment</b> interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemUnsecuredApartment</b> interface inherits from <b>IUnsecuredApartment</b>. <b>IWbemUnsecuredApartment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemUnsecuredApartment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/546ae2f8-c208-4846-a3ba-e124aefe619d">CreateSinkStub</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/546ae2f8-c208-4846-a3ba-e124aefe619d">CreateSinkStub</a> method is 
     similar to the 
     <a href="https://msdn.microsoft.com/76a376e4-bd0d-4b8b-b49a-162630c47220">IUnsecuredApartment::CreateObjectStub</a> 
     method. It creates an object forwarder sink and performs access checks for receiving asynchronous calls from 
     WMI.

</td>
</tr>
</table> 


## -remarks



<b>IWbemUnsecuredApartment</b> is similar to 
     <a href="https://msdn.microsoft.com/6293d8e3-cc5b-4401-8fdc-86f5d03720ea">IUnsecuredApartment</a>, which also creates a sink in a 
     separate process. For more information, see 
     <a href="https://msdn.microsoft.com/d0259bb1-fd74-4440-ac2a-d6aa84a48d9b">Performing Access Checks</a>.


<b>HKEY_LOCAL_MACHINE</b>\<b>SOFTWARE</b>\<b>Microsoft</b>\<b>WBEM</b>\<b>CIMOM</b>\<b>UnsecAppAccessControlDefault</b>






## -see-also




<a href="https://msdn.microsoft.com/6293d8e3-cc5b-4401-8fdc-86f5d03720ea">IUnsecuredApartment</a>



<a href="https://msdn.microsoft.com/3d3111ac-7d83-48d6-94e4-36cb46a506fa">Lowering the Security for a Sink in a Separate Process</a>



<a href="https://msdn.microsoft.com/d0259bb1-fd74-4440-ac2a-d6aa84a48d9b">Performing Access Checks</a>



<a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>
 

 

