---
UID: NS:ehstorapi._ACT_AUTHORIZATION_STATE
title: ACT_AUTHORIZATION_STATE (ehstorapi.h)
description: ACT_AUTHORIZATION_STATE structure contains data that describes the current authorization state of a Addressable Command Target (ACT).
helpviewer_keywords: ["ACT_AUTHORIZATION_STATE","ACT_AUTHORIZATION_STATE structure [Enhanced Storage]","PACT_AUTHORIZATION_STATE","PACT_AUTHORIZATION_STATE structure pointer [Enhanced Storage]","ehstorapi/ACT_AUTHORIZATION_STATE","ehstorapi/PACT_AUTHORIZATION_STATE","enstor.act_authorization_state"]
old-location: enstor\act_authorization_state.htm
tech.root: enstor
ms.assetid: 385b2f9d-659e-451d-97da-15be70180e1f
ms.date: 12/05/2018
ms.keywords: ACT_AUTHORIZATION_STATE, ACT_AUTHORIZATION_STATE structure [Enhanced Storage], PACT_AUTHORIZATION_STATE, PACT_AUTHORIZATION_STATE structure pointer [Enhanced Storage], ehstorapi/ACT_AUTHORIZATION_STATE, ehstorapi/PACT_AUTHORIZATION_STATE, enstor.act_authorization_state
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ACT_AUTHORIZATION_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ACT_AUTHORIZATION_STATE
 - ehstorapi/_ACT_AUTHORIZATION_STATE
 - ACT_AUTHORIZATION_STATE
 - ehstorapi/ACT_AUTHORIZATION_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EhStorAPI.h
api_name:
 - ACT_AUTHORIZATION_STATE
---

# ACT_AUTHORIZATION_STATE structure


## -description

The <b>ACT_AUTHORIZATION_STATE</b> structure contains data that describes the current authorization state of a Addressable Command Target (ACT).

## -struct-fields

### -field ulState

Integer value that indicates the possible authorization state of the ACT.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The ACT is unauthorized

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The ACT is authorized

</td>
</tr>
</table>

