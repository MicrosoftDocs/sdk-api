---
UID: NE:rend.RND_ADVERTISING_SCOPE
title: RND_ADVERTISING_SCOPE (rend.h)
author: windows-sdk-content
description: Members of the RND_ADVERTISING_SCOPE enumeration specify how widely a conference announcement is distributed. Values correspond to the advertising scope property on the ITDirectoryObjectConference interface.
old-location: tapi3\rnd_advertising_scope.htm
tech.root: Tapi
ms.assetid: e08e7b8a-e27b-48a8-ab2d-d4ce5fed912a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RAS_LOCAL, RAS_REGION, RAS_SITE, RAS_WORLD, RND_ADVERTISING_SCOPE, RND_ADVERTISING_SCOPE enumeration [TAPI 2.2], _tapi3_rnd_advertising_scope, rend/RAS_LOCAL, rend/RAS_REGION, rend/RAS_SITE, rend/RAS_WORLD, rend/RND_ADVERTISING_SCOPE, tapi3.rnd_advertising_scope
ms.topic: enum
req.header: rend.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rend.h
api_name:
 - RND_ADVERTISING_SCOPE
product: Windows
targetos: Windows
req.typenames: RND_ADVERTISING_SCOPE
req.redist: 
ms.custom: 19H1
---

# RND_ADVERTISING_SCOPE enumeration


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

Members of the 
<b>RND_ADVERTISING_SCOPE</b> enumeration specify how widely a conference announcement is distributed. Values correspond to the advertising scope property on the 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nn-rend-itdirectoryobjectconference">ITDirectoryObjectConference</a> interface.


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




<a href="https://docs.microsoft.com/windows/desktop/api/rend/nn-rend-itdirectoryobjectconference">ITDirectoryObjectConference</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_advertisingscope">get_AdvertisingScope</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-put_advertisingscope">put_AdvertisingScope</a>
 

 

