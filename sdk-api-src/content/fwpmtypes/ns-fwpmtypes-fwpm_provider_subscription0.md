---
UID: NS:fwpmtypes.FWPM_PROVIDER_SUBSCRIPTION0_
title: FWPM_PROVIDER_SUBSCRIPTION0 (fwpmtypes.h)
description: Used to subscribe for change notifications. (FWPM_PROVIDER_SUBSCRIPTION0)
helpviewer_keywords: ["FWPM_PROVIDER_SUBSCRIPTION0","FWPM_PROVIDER_SUBSCRIPTION0 structure [Filtering]","FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_ADD","FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE","fwp.fwpm_provider_subscription0_struct","fwpmtypes/FWPM_PROVIDER_SUBSCRIPTION0"]
old-location: fwp\fwpm_provider_subscription0_struct.htm
tech.root: fwp
ms.assetid: 651d9c40-50d4-407d-9d2a-4b7ad308150c
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_SUBSCRIPTION0, FWPM_PROVIDER_SUBSCRIPTION0 structure [Filtering], FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_ADD, FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE, fwp.fwpm_provider_subscription0_struct, fwpmtypes/FWPM_PROVIDER_SUBSCRIPTION0
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FWPM_PROVIDER_SUBSCRIPTION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_PROVIDER_SUBSCRIPTION0_
 - fwpmtypes/FWPM_PROVIDER_SUBSCRIPTION0_
 - FWPM_PROVIDER_SUBSCRIPTION0
 - fwpmtypes/FWPM_PROVIDER_SUBSCRIPTION0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_PROVIDER_SUBSCRIPTION0
---

# FWPM_PROVIDER_SUBSCRIPTION0 structure


## -description

The <b>FWPM_PROVIDER_SUBSCRIPTION0</b> structure is used to subscribe for change notifications.

## -struct-fields

### -field enumTemplate

[unique]

 Enumeration template for limiting the subscription.

See [FWPM_PROVIDER_ENUM_TEMPLATE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_enum_template0) for more information.

### -field flags

Possible values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_ADD"></a><a id="fwpm_subscription_flag_notify_on_add"></a><dl>
<dt><b>FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_ADD</b></dt>
</dl>
</td>
<td width="60%">
Subscribe to provider add notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE"></a><a id="fwpm_subscription_flag_notify_on_delete"></a><dl>
<dt><b>FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE</b></dt>
</dl>
</td>
<td width="60%">
Subscribe to provider delete notifications.

</td>
</tr>
</table>

### -field sessionKey

Uniquely identifies the session.

## -remarks

Notifications are only dispatched for providers that match the template.

If
   the template is <b>NULL</b>, it matches all providers.

<b>FWPM_PROVIDER_SUBSCRIPTION0</b> is a specific implementation of FWPM_PROVIDER_SUBSCRIPTION. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[FWPM_PROVIDER_ENUM_TEMPLATE0](/windows/desktop/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_enum_template0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
