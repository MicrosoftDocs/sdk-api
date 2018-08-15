---
UID: NS:ehstorapi._ACT_AUTHORIZATION_STATE
title: "_ACT_AUTHORIZATION_STATE"
author: windows-sdk-content
description: ACT_AUTHORIZATION_STATE structure contains data that describes the current authorization state of a Addressable Command Target (ACT).
old-location: enstor\act_authorization_state.htm
old-project: enstor
ms.assetid: 385b2f9d-659e-451d-97da-15be70180e1f
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ACT_AUTHORIZATION_STATE, ACT_AUTHORIZATION_STATE structure [Enhanced Storage], PACT_AUTHORIZATION_STATE, PACT_AUTHORIZATION_STATE structure pointer [Enhanced Storage], _ACT_AUTHORIZATION_STATE, ehstorapi/ACT_AUTHORIZATION_STATE, ehstorapi/PACT_AUTHORIZATION_STATE, enstor.act_authorization_state
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ehstorapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ACT_AUTHORIZATION_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - EhStorAPI.h
api_name:
 - ACT_AUTHORIZATION_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _ACT_AUTHORIZATION_STATE structure


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
 

