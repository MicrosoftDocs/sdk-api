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

# Provider::DeleteInstance(ParsedObjectPath,long,MethodContext)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class is part of the WMI 
    Provider Framework which is now considered in final state, and no further development, enhancements, or updates 
    will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>DeleteInstance</b> method is called by WMI to delete an instance.


## -parameters




### -param pParsedObjectPath




### -param lFlags

Bitmask of flags with information about the delete operation. This is the value specified by the client in the <a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">IWbemServices::DeleteInstance</a> function.

The following flag is handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
</ul>

### -param pContext






#### - Instance [ref]

Instance to be deleted.


## -returns



The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling function. The <a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">IWbemServices::DeleteInstance</a> function lists the most common return values, although you can choose to return any COM return code.




## -remarks



WMI invokes <b>DeleteInstance</b> when a client calls <a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">IWbemServices::DeleteInstance</a> against a class. Therefore, you must implement <b>DeleteInstance</b> if your framework provider supports deleting instances. The following list describes a common implementation of <b>DeleteInstance</b>:

<ol>
<li>Determine which instance the client requested by reading the key properties with one of the <b>Get</b> methods for <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a>, such as <a href="https://msdn.microsoft.com/d9295ba1-19da-41a2-86d1-ec80e18e895b">CInstance::GetCHString</a>.</li>
<li>Delete the instance.</li>
</ol>
For more information about deleting instances, see <a href="https://msdn.microsoft.com/f6dfeb1d-1730-4df4-adf7-f27dd9edc54d">IWbemServices::DeleteInstance</a>.



