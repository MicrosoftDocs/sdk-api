---
UID: NS:fwpmtypes.FWPM_FILTER_SUBSCRIPTION0_
title: FWPM_FILTER_SUBSCRIPTION0
author: windows-sdk-content
description: Is used to subscribe for change notifications.
old-location: fwp\fwpm_filter_subscription0_struct.htm
tech.root: fwp
ms.assetid: 723d2e27-420d-4eea-9ae1-d624807bf4ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FWPM_FILTER_SUBSCRIPTION0, FWPM_FILTER_SUBSCRIPTION0 structure [Filtering], FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_ADD, FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE, fwp.fwpm_filter_subscription0_struct, fwpmtypes/FWPM_FILTER_SUBSCRIPTION0
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
 - FWPM_FILTER_SUBSCRIPTION0
product: Windows
targetos: Windows
req.typenames: FWPM_FILTER_SUBSCRIPTION0
req.redist: 
---

# FWPM_FILTER_SUBSCRIPTION0 structure


## -description


The <b>FWPM_FILTER_SUBSCRIPTION0</b> structure is used to subscribe for change notifications.


## -struct-fields




### -field enumTemplate

A  <a href="https://msdn.microsoft.com/5ae77ee2-42b2-4794-afec-80360fe4f4da">FWPM_FILTER_ENUM_TEMPLATE0</a> structure used to limit the subscription.


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
Subscribe to filter add notifications.

</td>
</tr>
<tr>
<td width="40%"><a id="FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE"></a><a id="fwpm_subscription_flag_notify_on_delete"></a><dl>
<dt><b>FWPM_SUBSCRIPTION_FLAG_NOTIFY_ON_DELETE</b></dt>
</dl>
</td>
<td width="60%">
Subscribe to filter delete notifications.

</td>
</tr>
</table>
 


### -field sessionKey

Uniquely identifies this session.


## -remarks



Notifications are only dispatched for filters that match the template.

If
   the template is <b>NULL</b>, it matches all filters.

<b>FWPM_FILTER_SUBSCRIPTION0</b> is a specific implementation of FWPM_FILTER_SUBSCRIPTION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/5ae77ee2-42b2-4794-afec-80360fe4f4da">FWPM_FILTER_ENUM_TEMPLATE0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

