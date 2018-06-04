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

# RND_ADVERTISING_SCOPE enumeration


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

Members of the 
<b>RND_ADVERTISING_SCOPE</b> enumeration specify how widely a conference announcement is distributed. Values correspond to the advertising scope property on the 
<a href="https://msdn.microsoft.com/bab167cf-2726-4423-87b3-69227404bddc">ITDirectoryObjectConference</a> interface.


## -enum-fields




### -field RAS_LOCAL

Advertising scope is local.


### -field RAS_SITE

Advertising scope is site.


### -field RAS_REGION

Advertising scope is country or region.


### -field RAS_WORLD

Advertising scope is the world.


## -remarks



Mapping between scope string value, enum value, and 
<a href="../tapi2/t_tapgloss.htm">time to live</a> (TTL) based on SDP Internet draft.

<table>
<tr>
<th>Scope string value</th>
<th>RND_ADVERTISING_SCOPE</th>
<th>TTL</th>
</tr>
<tr>
<td>Local</td>
<td>AS_LOCAL</td>
<td>1</td>
</tr>
<tr>
<td>Site</td>
<td>AS_SITE</td>
<td>15</td>
</tr>
<tr>
<td>Region</td>
<td>AS_REGION</td>
<td>63</td>
</tr>
<tr>
<td>World</td>
<td>AS_WORLD</td>
<td>127</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/bab167cf-2726-4423-87b3-69227404bddc">ITDirectoryObjectConference</a>



<a href="https://msdn.microsoft.com/25e155ad-c809-4ff4-85cb-ca43cb203368">get_AdvertisingScope</a>



<a href="https://msdn.microsoft.com/74d7c770-e11d-4d87-acdb-821d64feed0c">put_AdvertisingScope</a>
 

 

