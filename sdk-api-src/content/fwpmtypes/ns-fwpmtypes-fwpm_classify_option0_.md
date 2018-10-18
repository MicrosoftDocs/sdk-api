---
UID: NS:fwpmtypes.FWPM_CLASSIFY_OPTION0_
title: FWPM_CLASSIFY_OPTION0_
author: windows-sdk-content
description: The FWPM_CLASSIFY_OPTION0 structure can be used to define unicast and multicast time-out options and data for a non-TCP state.Note  FWPM_CLASSIFY_OPTION0 is a specific version of FWPM_CLASSIFY_OPTION.
old-location: netvista\fwpm_classify_option0.htm
tech.root: NetVista
ms.assetid: 2ffc121d-9b57-4935-9784-12447d2e0c46
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWPM_CLASSIFY_OPTION0, FWPM_CLASSIFY_OPTION0 structure [Network Drivers Starting with Windows Vista], FWPM_CLASSIFY_OPTION0_, fwpmtypes/FWPM_CLASSIFY_OPTION0, netvista.fwpm_classify_option0, wfp_ref_3_struct_2_fwpm_A-Z_8cb94183-c769-41de-a3af-53c2710b2684.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: Fwpmk.h
req.target-type: Windows
req.target-min-winverclnt: Available starting with Windows Vista.
req.target-min-winversvr: 
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
 - fwpmtypes.h
api_name:
 - FWPM_CLASSIFY_OPTION0
product: Windows
targetos: Windows
req.typenames: FWPM_CLASSIFY_OPTION0
req.redist: 
---

# FWPM_CLASSIFY_OPTION0_ structure


## -description


The <b>FWPM_CLASSIFY_OPTION0</b> structure can be used to define unicast and multicast time-out options and
  data for a non-TCP state.
<div class="alert"><b>Note</b>  <b>FWPM_CLASSIFY_OPTION0</b> is a specific version of <b>FWPM_CLASSIFY_OPTION</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field type

An 
     <a href="https://msdn.microsoft.com/4731b03d-4c51-414b-a07d-0957b9a04db2">FWP_CLASSIFY_OPTION_TYPE</a> value that
     specifies unicast, multicast, or loose source mapping options, or data time-out values.


### -field value

An 
     <a href="https://msdn.microsoft.com/0d8557cd-bd11-4786-ba6e-fbbeb2e2b761">FWP_VALUE0</a> value that specifies the value of the
     data lifetime.


## -remarks



The 
    <a href="https://msdn.microsoft.com/ee50e09b-1a06-412e-a7d4-0ecdbb053990">FWPM_CLASSIFY_OPTIONS0</a> structure can
    be used to define multiple settings of this structure.




## -see-also




<a href="https://msdn.microsoft.com/ee50e09b-1a06-412e-a7d4-0ecdbb053990">FWPM_CLASSIFY_OPTIONS0</a>



<a href="https://msdn.microsoft.com/4731b03d-4c51-414b-a07d-0957b9a04db2">FWP_CLASSIFY_OPTION_TYPE</a>
 

 

