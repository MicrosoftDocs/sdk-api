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

# FWPM_CALLOUT0_ structure


## -description


The <b>FWPM_CALLOUT0</b> structure stores the state associated with a callout.


## -struct-fields




### -field calloutKey

Uniquely identifies the session. 

If the GUID is initialized to zero in the
   call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff550067">FwpmCalloutAdd0</a>, the base filtering engine (BFE) will generate one.


### -field displayData

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff550081">FWPM_DISPLAY_DATA0</a> structure that contains human-readable annotations associated with the callout.  The <b>name</b> member of the <b>FWPM_DISPLAY_DATA0</b> structure is required.


### -field flags

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_CALLOUT_FLAG_PERSISTENT"></a><a id="fwpm_callout_flag_persistent"></a><dl>
<dt><b>FWPM_CALLOUT_FLAG_PERSISTENT</b></dt>
</dl>
</td>
<td width="60%">
The callout is persistent across reboots. As a result, it can be referenced by boot-time and other persistent filters.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_CALLOUT_FLAG_USES_PROVIDER_CONTEXT"></a><a id="fwpm_callout_flag_uses_provider_context"></a><dl>
<dt><b>FWPM_CALLOUT_FLAG_USES_PROVIDER_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
The callout needs access to the provider context stored in the filter invoking the callout.  If this flag is set, the provider context will be copied from the <a href="https://msdn.microsoft.com/e1925824-01c2-426a-a8f0-4d5882812a9e">FWPM_FILTER0</a> structure to the <b>FWPS_FILTER0</b> 
structure. The <b>FWPS_FILTER0</b> structure is documented in the WDK.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_CALLOUT_FLAG_REGISTERED"></a><a id="fwpm_callout_flag_registered"></a><dl>
<dt><b>FWPM_CALLOUT_FLAG_REGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The callout is currently registered in the kernel.  This flag must not be set when adding new callouts.  It is used only in querying the state of existing callouts.

</td>
</tr>
</table>
 


### -field providerKey

Uniquely identifies the provider associated with the callout. If the member is non-NULL, only objects associated with the specified provider will be returned.


### -field providerData

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> structure that contains optional provider-specific data that allows providers to store additional context information with the object.


### -field applicableLayer

Specifies the layer in which the callout can be used. Only filters in this layer can invoke the callout. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff549947">Filtering Layer Identifiers</a>.


### -field calloutId

   LUID identifying the callout. This is the <b>calloutId</b> stored in the
   <b>FWPS_ACTION0</b> structure for filters that invoke a callout. The <b>FWPS_ACTION0</b> structure is documented in the WDK.


## -remarks



The first six members of this structure contain data supplied when adding objects.

The last member, <b>calloutId</b>, provides additional information returned when getting/enumerating objects.

<b>FWPM_CALLOUT0</b> is a specific implementation of FWPM_CALLOUT. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

