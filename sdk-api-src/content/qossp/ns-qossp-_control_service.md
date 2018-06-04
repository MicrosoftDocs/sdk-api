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

# _CONTROL_SERVICE structure


## -description


The <b>CONTROL_SERVICE</b> structure contains supported RSVP service types.


## -struct-fields




### -field Length

Length of the entire structure, in bytes.


### -field Service

The supported service type. Must be one of the following:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NOTRAFFIC"></a><a id="servicetype_notraffic"></a><dl>
<dt><b>SERVICETYPE_NOTRAFFIC</b></dt>
</dl>
</td>
<td width="60%">
No data is being sent in this direction.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_BESTEFFORT"></a><a id="servicetype_besteffort"></a><dl>
<dt><b>SERVICETYPE_BESTEFFORT</b></dt>
</dl>
</td>
<td width="60%">
Best Effort service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_CONTROLLEDLOAD"></a><a id="servicetype_controlledload"></a><dl>
<dt><b>SERVICETYPE_CONTROLLEDLOAD</b></dt>
</dl>
</td>
<td width="60%">
Controlled Load service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_GUARANTEED"></a><a id="servicetype_guaranteed"></a><dl>
<dt><b>SERVICETYPE_GUARANTEED</b></dt>
</dl>
</td>
<td width="60%">
Guaranteed service.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NETWORK_UNAVAILABLE"></a><a id="servicetype_network_unavailable"></a><dl>
<dt><b>SERVICETYPE_NETWORK_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
This service type is used to notify the user that the network is unavailable.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_GENERAL_INFORMATION"></a><a id="servicetype_general_information"></a><dl>
<dt><b>SERVICETYPE_GENERAL_INFORMATION</b></dt>
</dl>
</td>
<td width="60%">
This service type corresponds to General Parameters, as defined by IntServ (the Integrated Services Working Group in the IETF).

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NOCHANGE"></a><a id="servicetype_nochange"></a><dl>
<dt><b>SERVICETYPE_NOCHANGE</b></dt>
</dl>
</td>
<td width="60%">
This specifies that the flow specification contains no changes from the previous specification.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NONCONFORMING"></a><a id="servicetype_nonconforming"></a><dl>
<dt><b>SERVICETYPE_NONCONFORMING</b></dt>
</dl>
</td>
<td width="60%">
Specifies non-conforming traffic.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_NETWORK_CONTROL"></a><a id="servicetype_network_control"></a><dl>
<dt><b>SERVICETYPE_NETWORK_CONTROL</b></dt>
</dl>
</td>
<td width="60%">
Specifies network control traffic.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICETYPE_QUALITATIVE"></a><a id="servicetype_qualitative"></a><dl>
<dt><b>SERVICETYPE_QUALITATIVE</b></dt>
</dl>
</td>
<td width="60%">
Qualitative service.

</td>
</tr>
</table>
 


### -field Overrides

Specifies overrides to service specifications, expressed in the form of an <a href="https://msdn.microsoft.com/eab6b317-9d06-45e2-bc77-0882f40e7d79">AD_GENERAL_PARAMS</a> structure.


### -field Guaranteed

Specifies guaranteed service, and provides service parameters in the form of an <b>AD_GUARANTEED</b> structure.


### -field ParamBuffer

Describes the buffer used, in the form of a <a href="https://msdn.microsoft.com/b5078f3b-ab7f-4194-aed7-de5ebb4f7fb8">PARAM_BUFFER</a> structure.


## -remarks



The <b>Length</b> value can be added to the pointer to the structure to obtain the pointer to the next <b>CONTROL_SERVICE</b> structure in the list, until the <b>NumberOfServices</b> member of the <a href="https://msdn.microsoft.com/90fad5de-7105-4126-a6db-d4fb663e01f4">RSVP_ADSPEC</a> structure is exhausted.




## -see-also




<a href="https://msdn.microsoft.com/b5078f3b-ab7f-4194-aed7-de5ebb4f7fb8">PARAM_BUFFER</a>



<a href="https://msdn.microsoft.com/90fad5de-7105-4126-a6db-d4fb663e01f4">RSVP_ADSPEC</a>
 

 

