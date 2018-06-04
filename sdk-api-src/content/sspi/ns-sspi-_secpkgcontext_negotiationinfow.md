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

# _SecPkgContext_NegotiationInfoW structure


## -description


The <b>SecPkgContext_NegotiationInfo</b> structure contains information on the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> that is being set up or has been set up, and also gives the status on the negotiation to set up the security package.


## -struct-fields




### -field PackageInfo

Pointer to a 
<a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a> structure that provides general information about the security package chosen in the negotiate process, such as the name and capabilities of the package.


### -field NegotiationState

Indicator of the state of the negotiation for the security package identified in the <b>PackageInfo</b> member. This attribute can be queried from the context handle before the setup is complete, such as when ISC returns SEC_I_CONTINUE_NEEDED.

The following table shows values returned in this member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECPKG_NEGOTIATION_COMPLETE"></a><a id="secpkg_negotiation_complete"></a><dl>
<dt><b>SECPKG_NEGOTIATION_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
Negotiation has been completed.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_NEGOTIATION_OPTIMISTIC"></a><a id="secpkg_negotiation_optimistic"></a><dl>
<dt><b>SECPKG_NEGOTIATION_OPTIMISTIC</b></dt>
</dl>
</td>
<td width="60%">
Negotiations not yet completed.

</td>
</tr>
<tr>
<td width="40%"><a id="SECPKG_NEGOTIATION_IN_PROGRESS"></a><a id="secpkg_negotiation_in_progress"></a><dl>
<dt><b>SECPKG_NEGOTIATION_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
Negotiations in progress.

</td>
</tr>
</table>
 

