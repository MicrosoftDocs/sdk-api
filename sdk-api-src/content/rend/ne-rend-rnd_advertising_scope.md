---
UID: NE:rend.RND_ADVERTISING_SCOPE
title: RND_ADVERTISING_SCOPE (rend.h)
description: Members of the RND_ADVERTISING_SCOPE enumeration specify how widely a conference announcement is distributed. Values correspond to the advertising scope property on the ITDirectoryObjectConference interface.
helpviewer_keywords: ["RAS_LOCAL","RAS_REGION","RAS_SITE","RAS_WORLD","RND_ADVERTISING_SCOPE","RND_ADVERTISING_SCOPE enumeration [TAPI 2.2]","_tapi3_rnd_advertising_scope","rend/RAS_LOCAL","rend/RAS_REGION","rend/RAS_SITE","rend/RAS_WORLD","rend/RND_ADVERTISING_SCOPE","tapi3.rnd_advertising_scope"]
old-location: tapi3\rnd_advertising_scope.htm
tech.root: tapi3
ms.assetid: e08e7b8a-e27b-48a8-ab2d-d4ce5fed912a
ms.date: 12/05/2018
ms.keywords: RAS_LOCAL, RAS_REGION, RAS_SITE, RAS_WORLD, RND_ADVERTISING_SCOPE, RND_ADVERTISING_SCOPE enumeration [TAPI 2.2], _tapi3_rnd_advertising_scope, rend/RAS_LOCAL, rend/RAS_REGION, rend/RAS_SITE, rend/RAS_WORLD, rend/RND_ADVERTISING_SCOPE, tapi3.rnd_advertising_scope
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
targetos: Windows
req.typenames: RND_ADVERTISING_SCOPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RND_ADVERTISING_SCOPE
 - rend/RND_ADVERTISING_SCOPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rend.h
api_name:
 - RND_ADVERTISING_SCOPE
---

# RND_ADVERTISING_SCOPE enumeration


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

Members of the 
<b>RND_ADVERTISING_SCOPE</b> enumeration specify how widely a conference announcement is distributed. Values correspond to the advertising scope property on the 
<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobjectconference">ITDirectoryObjectConference</a> interface.

## -enum-fields

### -field RAS_LOCAL:1

Advertising scope is local.

### -field RAS_SITE:2

Advertising scope is site.

### -field RAS_REGION:3

Advertising scope is country or region.

### -field RAS_WORLD:4

Advertising scope is the world.

## -remarks

Mapping between scope string value, enum value, and 
<a href="/windows/win32/tapi/t-tapgloss">time to live</a> (TTL) based on SDP Internet draft.

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

<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobjectconference">ITDirectoryObjectConference</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-get_advertisingscope">get_AdvertisingScope</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobjectconference-put_advertisingscope">put_AdvertisingScope</a>
