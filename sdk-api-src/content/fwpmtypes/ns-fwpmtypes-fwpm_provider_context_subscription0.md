---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0_
title: FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0 (fwpmtypes.h)
description: Used to subscribe for change notifications.
helpviewer_keywords: ["FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0","FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0 structure [Filtering]","FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_ADD","FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE","fwp.fwpm_provider_context_subscription0_struct","fwpmtypes/FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0"]
old-location: fwp\fwpm_provider_context_subscription0_struct.htm
tech.root: fwp
ms.assetid: 44c01600-7cb6-45f4-a2e1-746f200ee772
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0, FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0 structure [Filtering], FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_ADD, FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE, fwp.fwpm_provider_context_subscription0_struct, fwpmtypes/FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0
f1_keywords:
- fwpmtypes/FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Fwpmtypes.h
api_name:
- FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0
targetos: Windows
req.typenames: FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0
req.redist: 
ms.custom: 19H1
---

# FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0 structure


## -description


The <b>FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0</b> structure is  used to subscribe for change notifications.


## -struct-fields




### -field enumTemplate

Notifications are only dispatched for objects that match the template. If the template is <b>NULL</b>, it matches all objects.

See <a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0">FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</a> for more information


### -field flags

The notifications to subscribe to, as one of the following values.

<table>
<tr>
<th>Subscription flag</th>
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

Uniquely identifies this session.


## -remarks



<b>FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0</b> is a specific implementation of FWPM_PROVIDER_CONTEXT_SUBSCRIPTION. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context_enum_template0">FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

