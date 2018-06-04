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

# Provider::EnumerateInstances


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>EnumerateInstances</b> method is called by WMI to retrieve all instances of a framework provider's class.


## -parameters




### -param pMethodContext

Pointer to the context object for this call. This value contains any <a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> properties specified by the client. Also, this pointer must be used as a parameter to any calls back into WMI.


### -param lFlags

Bitmask of flags with information about the <b>EnumerateInstances</b> operation. This is the value specified by the client in the <a href="https://msdn.microsoft.com/47671b9b-a2ff-4375-b2a4-7e8599f1fb69">IWbemServices::CreateInstanceEnum</a> method.

The following flags are handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_DEEP</b></li>
<li><b>WBEM_FLAG_SHALLOW</b></li>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
<li><b>WBEM_FLAG_FORWARD_ONLY</b></li>
<li><b>WBEM_FLAG_BIDIRECTIONAL</b></li>
<li><b>WBEM_FLAG_USE_AMENDED_QUALIFIERS</b></li>
</ul>

## -returns



The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling method. The <a href="https://msdn.microsoft.com/47671b9b-a2ff-4375-b2a4-7e8599f1fb69">IWbemServices::CreateInstanceEnum</a> method lists the most common return values, but you can choose to return any COM return code.




## -remarks



It is not an error for <b>EnumerateInstances</b> to return zero instances by instantiating zero <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> instances and setting the return value to <b>WBEM_S_NO_ERROR</b>.

WMI often calls <b>EnumerateInstances</b> when a client application calls <a href="https://msdn.microsoft.com/47671b9b-a2ff-4375-b2a4-7e8599f1fb69">IWbemServices::CreateInstanceEnum</a>, although WMI may call <b>EnumerateInstances</b> in other situations as well. The following is a common way to override <b>EnumerateInstances</b>:

<ol>
<li>Create an empty instance of your class using <a href="https://msdn.microsoft.com/cb520b55-9ef8-4f5a-935d-46c2bb01f5dd">Provider::CreateNewInstance</a>.</li>
<li>Populate the properties of the empty instance using the Set methods of the <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class, such as <a href="https://msdn.microsoft.com/d6ecbada-4eb6-40ad-9e59-ba77fd3b883a">CInstance::SetByte</a> or <a href="https://msdn.microsoft.com/dcd1e108-4914-43ea-aa41-d38d38e8954a">CInstance::SetStringArray</a>.</li>
<li>Send the instance back to the client using <a href="https://msdn.microsoft.com/699dadf9-18b5-4c6d-a5c4-59ea8a85f089">CInstance::Commit</a>.</li>
</ol>
If you are building a method-only provider and do not have any instances, or if enumerating instances of your class would return too many instances, you may decide to support queries that retrieve only specific instances.



