---
UID: NS:fwpmtypes.FWPM_CALLOUT_SUBSCRIPTION0_
title: FWPM_CALLOUT_SUBSCRIPTION0_
author: windows-sdk-content
description: Used to subscribe for change notifications.
old-location: fwp\fwpm_callout_subscription0_struct.htm
tech.root: fwp
ms.assetid: 35afdc09-0745-4d59-9be1-d360b02fbd2f
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: FWPM_CALLOUT_SUBSCRIPTION0, FWPM_CALLOUT_SUBSCRIPTION0 structure [Filtering], FWPM_CALLOUT_SUBSCRIPTION0_, FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_ADD, FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE, fwp.fwpm_callout_subscription0_struct, fwpmtypes/FWPM_CALLOUT_SUBSCRIPTION0
ms.prod: windows
ms.technology: windows-sdk
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
 - FWPM_CALLOUT_SUBSCRIPTION0
product: Windows
targetos: Windows
req.typenames: FWPM_CALLOUT_SUBSCRIPTION0
req.redist: 
---

# FWPM_CALLOUT_SUBSCRIPTION0_ structure


## -description


The <b>FWPM_CALLOUT_SUBSCRIPTION0</b> structure is used to subscribe for change notifications.


## -struct-fields




### -field enumTemplate

 A <a href="https://msdn.microsoft.com/10997be6-069d-4d1a-a6b1-1a1e0a5359c5">FWPM_CALLOUT_ENUM_TEMPLATE0</a> structure that is used to limit the subscription.


### -field flags

The notification type(s) received by the subscription.

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
Subscribe to callout add notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE"></a><a id="fwpm_subscription_flag_notify_on_delete"></a><dl>
<dt><b>FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE</b></dt>
</dl>
</td>
<td width="60%">
Subscribe to callout delete notifications.

</td>
</tr>
</table>
 


### -field sessionKey

Uniquely identifies this session.


## -remarks



Notifications are only dispatched for callouts that match the template. 

If
   the template is <b>NULL</b>, it matches all callouts.

<b>FWPM_CALLOUT_SUBSCRIPTION0</b> is a specific implementation of FWPM_CALLOUT_SUBSCRIPTION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/10997be6-069d-4d1a-a6b1-1a1e0a5359c5">FWPM_CALLOUT_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

