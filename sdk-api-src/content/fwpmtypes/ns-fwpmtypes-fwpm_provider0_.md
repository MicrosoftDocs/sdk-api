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

# FWPM_PROVIDER0_ structure


## -description


The <b>FWPM_PROVIDER0</b> structure stores the state associated with a policy provider.


## -struct-fields




### -field providerKey

Uniquely identifies the provider. 

If the GUID is zero-initialized in the
   call to Add, Base Filtering Engine (BFE) will generate one.


### -field displayData

Allows providers to be annotated in a human-readable form.  The <b>name</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550081">FWPM_DISPLAY_DATA0</a> structure is required.


### -field flags

Bit flags that indicate information about the persistence of the provider.

<table>
<tr>
<th>Provider flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_PROVIDER_FLAG_PERSISTENT"></a><a id="fwpm_provider_flag_persistent"></a><dl>
<dt><b>FWPM_PROVIDER_FLAG_PERSISTENT</b></dt>
</dl>
</td>
<td width="60%">
Provider is persistent.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_PROVIDER_FLAG_DISABLED"></a><a id="fwpm_provider_flag_disabled"></a><dl>
<dt><b>FWPM_PROVIDER_FLAG_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Provider's filters were disabled when the BFE started because the provider has no associated Windows service name, or because the associated service was not set to auto-start. 

<div class="alert"><b>Note</b>  This flag cannot be set when adding new providers. It can only be returned by BFE when getting or enumerating providers.</div>
<div> </div>
</td>
</tr>
</table>
 


### -field providerData

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> structure that contains optional provider-specific data that allows providers to store additional context info with the object.


### -field serviceName

Optional name of the Windows service hosting the provider. This allows
   BFE to detect that a provider has been disabled.


## -remarks



<b>FWPM_PROVIDER0</b> is a specific implementation of FWPM_PROVIDER. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550081">FWPM_DISPLAY_DATA0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

