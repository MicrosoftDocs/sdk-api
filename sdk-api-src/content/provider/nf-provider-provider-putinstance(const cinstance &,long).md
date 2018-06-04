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

# Provider::PutInstance(const CInstance &,long)


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class is part of the WMI 
    Provider Framework which is now considered in final state, and no further development, enhancements, or updates 
    will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>PutInstance</b> method updates an instance.


## -parameters




### -param newInstance [ref]

Instance that is updated.


### -param lFlags

Bitmask of flags with information about the update operation. This is the value specified by the client in the <a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a> method.

The following flag is handled by (and filtered out) by WMI:

<ul>
<li><b>WBEM_FLAG_RETURN_IMMEDIATELY</b></li>
</ul>
Valid <i>lFlags</i> values are:

<ul>
<li><b>WBEM_FLAG_CREATE_ONLY</b></li>
<li><b>WBEM_FLAG_CREATE_OR_UPDATE</b></li>
<li><b>WBEM_FLAG_UPDATE_ONLY</b></li>
</ul>

## -returns



The default framework provider implementation of this method returns <b>WBEM_E_PROVIDER_NOT_CAPABLE</b> to the calling method. The <a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a> method lists the most common return values, although you can choose to return any COM return code.




## -remarks



WMI invokes <b>PutInstance</b> when a client calls <a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a> against your class. You must implement <b>PutInstance</b> if your framework provider updates instances. The following list describes a common implementation of <b>PutInstance</b>:

<ol>
<li>
Examine the key properties passed in by the client with the Get methods for <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a>, such as <a href="https://msdn.microsoft.com/d9295ba1-19da-41a2-86d1-ec80e18e895b">CInstance::GetCHString</a>.

Your implementation should determine if your provider supports the changes requested by the client.

</li>
<li>Create or update the appropriate managed object, as necessary.</li>
<li>
Return the appropriate return value.

If your provider does not support the changes requested by the client, you should return an appropriate error code. For a complete listing of valid error codes, see <a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a>.

</li>
</ol>


