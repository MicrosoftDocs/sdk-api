---
UID: NS:fwpmtypes.FWPM_VSWITCH_EVENT_SUBSCRIPTION0_
title: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
author: windows-sdk-content
description: Stores information used to subscribe to notifications about a vSwitch event.
old-location: fwp\fwpm_vswitch_event_subscription0.htm
tech.root: fwp
ms.assetid: f099d531-ab40-4661-b33f-a805a84fba7e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FWPM_VSWITCH_EVENT_SUBSCRIPTION0, FWPM_VSWITCH_EVENT_SUBSCRIPTION0 structure [Filtering], fwp.fwpm_vswitch_event_subscription0, fwpmtypes/FWPM_VSWITCH_EVENT_SUBSCRIPTION0
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
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
 - FWPM_VSWITCH_EVENT_SUBSCRIPTION0
product: Windows
targetos: Windows
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
req.redist: 
---

# FWPM_VSWITCH_EVENT_SUBSCRIPTION0 structure


## -description


The <b>FWPM_VSWITCH_EVENT_SUBSCRIPTION0</b> structure stores information used to subscribe to notifications about a vSwitch event.


## -struct-fields




### -field flags

Type: <b>UINT32</b>

This member is reserved for future use.


### -field sessionKey

Type: <b>GUID</b>

Identifies the session which created the subscription.


## -remarks



<b>FWPM_VSWITCH_EVENT_SUBSCRIPTION0</b> is a specific implementation of FWPM_VSWITCH_EVENT_SUBSCRIPTION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/1264a58d-81e1-4877-915d-6ed3d7d15512">FwpmvSwitchEventSubscribe0</a>
 

 

