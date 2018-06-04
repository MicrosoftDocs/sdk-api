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

# FWPM_SUBLAYER0_ structure


## -description


The <b>FWPM_SUBLAYER0</b> structure stores the state associated with a sublayer.


## -struct-fields




### -field subLayerKey

Uniquely identifies the sublayer. See <a href="https://msdn.microsoft.com/4c8dbe35-e84b-4490-bf7a-7ff8b94e2022">Filtering Sublayer Identifiers</a> for a list of built-in sublayers.

If the GUID is zero-initialized in the call to <a href="https://msdn.microsoft.com/85a6f4a9-297f-491d-b2f7-38de21dbe06c">FwpmSubLayerAdd0</a>, the Base Filtering Engine (BFE) will generate one.


### -field displayData

Allows sublayers to be annotated in human-readable form.   The <b>name</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550081">FWPM_DISPLAY_DATA0</a> structure is required.


### -field flags

Possible values:

<table>
<tr>
<th>Sublayer flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_SUBLAYER_FLAG_PERSISTENT"></a><a id="fwpm_sublayer_flag_persistent"></a><dl>
<dt><b>FWPM_SUBLAYER_FLAG_PERSISTENT</b></dt>
</dl>
</td>
<td width="60%">
Causes sublayer to be persistent, surviving across BFE stop/start.

</td>
</tr>
</table>
 


### -field providerKey

Uniquely identifies the provider that manages this sublayer.


### -field providerData

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> structure that contains optional provider-specific data that allows providers to store additional context info with the object.


### -field weight

Weight of the sublayer. 

Higher-weighted sublayers are invoked first.


## -remarks



<b>FWPM_SUBLAYER0</b> is a specific implementation of FWPM_SUBLAYER. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

