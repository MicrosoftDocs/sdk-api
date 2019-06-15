---
UID: NS:fwpmtypes.FWPM_PROVIDER_CHANGE0_
title: FWPM_PROVIDER_CHANGE0 (fwpmtypes.h)
author: windows-sdk-content
description: Change notification dispatched to subscribers.
old-location: fwp\fwpm_provider_change0_struct.htm
tech.root: fwp
ms.assetid: abd5c40c-5907-4f1e-8fb3-28d43ecebfc8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_PROVIDER_CHANGE0, FWPM_PROVIDER_CHANGE0 structure [Filtering], fwp.fwpm_provider_change0_struct, fwpmtypes/FWPM_PROVIDER_CHANGE0
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
 - FWPM_PROVIDER_CHANGE0
product: Windows
targetos: Windows
req.typenames: FWPM_PROVIDER_CHANGE0
req.redist: 
ms.custom: 19H1
---

# FWPM_PROVIDER_CHANGE0 structure


## -description


The <b>FWPM_PROVIDER_CHANGE0</b> structure specifies a change notification dispatched to subscribers.


## -struct-fields




### -field changeType

Type of change.

See <a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_change_type_">FWPM_CHANGE_TYPE</a> for more information.


### -field providerKey

GUID of the provider that changed.


## -remarks



<b>FWPM_PROVIDER_CHANGE0</b> is a specific implementation of FWPM_PROVIDER_CHANGE. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmtypes/ne-fwpmtypes-fwpm_change_type_">FWPM_CHANGE_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

