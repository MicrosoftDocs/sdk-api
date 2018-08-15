---
UID: NS:fwpmtypes.FWPM_PROVIDER_SUBSCRIPTION0_
title: FWPM_PROVIDER_SUBSCRIPTION0_
author: windows-sdk-content
description: Used to subscribe for change notifications.
old-location: fwp\fwpm_provider_subscription0_struct.htm
old-project: fwp
ms.assetid: 651d9c40-50d4-407d-9d2a-4b7ad308150c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FWPM_PROVIDER_SUBSCRIPTION0, FWPM_PROVIDER_SUBSCRIPTION0 structure [Filtering], FWPM_PROVIDER_SUBSCRIPTION0_, FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_ADD, FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE, fwp.fwpm_provider_subscription0_struct, fwpmtypes/FWPM_PROVIDER_SUBSCRIPTION0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FWPM_PROVIDER_SUBSCRIPTION0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_PROVIDER_SUBSCRIPTION0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPM_PROVIDER_SUBSCRIPTION0_ structure


## -description


The <b>FWPM_PROVIDER_SUBSCRIPTION0</b> structure is used to subscribe for change notifications.


## -struct-fields




### -field enumTemplate

[unique]

 Enumeration template for limiting the subscription.

See <a href="https://msdn.microsoft.com/9369becc-f766-444a-8056-a3c3bc610553">FWPM_PROVIDER_ENUM_TEMPLATE0</a> for more information.


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

<b>FWPM_PROVIDER_SUBSCRIPTION0</b> is a specific implementation of FWPM_PROVIDER_SUBSCRIPTION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/9369becc-f766-444a-8056-a3c3bc610553">FWPM_PROVIDER_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

