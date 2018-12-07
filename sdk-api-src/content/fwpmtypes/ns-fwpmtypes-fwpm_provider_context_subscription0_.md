---
UID: NS:fwpmtypes.FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0_
title: FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0_
author: windows-sdk-content
description: Used to subscribe for change notifications.
old-location: fwp\fwpm_provider_context_subscription0_struct.htm
tech.root: fwp
ms.assetid: 44c01600-7cb6-45f4-a2e1-746f200ee772
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0, FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0 structure [Filtering], FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0_, FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_ADD, FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE, fwp.fwpm_provider_context_subscription0_struct, fwpmtypes/FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0
req.redist: 
---

# FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0_ structure


## -description


The <b>FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0</b> structure is  used to subscribe for change notifications.


## -struct-fields




### -field enumTemplate

Notifications are only dispatched for objects that match the template. If the template is <b>NULL</b>, it matches all objects.

See <a href="https://msdn.microsoft.com/0d43931a-93ae-43dd-9c5b-3989799e7b60">FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</a> for more information


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



<b>FWPM_PROVIDER_CONTEXT_SUBSCRIPTION0</b> is a specific implementation of FWPM_PROVIDER_CONTEXT_SUBSCRIPTION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/0d43931a-93ae-43dd-9c5b-3989799e7b60">FWPM_PROVIDER_CONTEXT_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

