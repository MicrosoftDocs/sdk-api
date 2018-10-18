---
UID: NS:fwpmtypes.FWPM_CLASSIFY_OPTIONS0_
title: FWPM_CLASSIFY_OPTIONS0_
author: windows-sdk-content
description: The FWPM_CLASSIFY_OPTIONS0 structure can be used to define multiple time-out options and data for use with the FwpsClassifyOptionSet0 function.Note  FWPM_CLASSIFY_OPTIONS0 is a specific version of FWPM_CLASSIFY_OPTIONS.
old-location: netvista\fwpm_classify_options0.htm
tech.root: NetVista
ms.assetid: ee50e09b-1a06-412e-a7d4-0ecdbb053990
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWPM_CLASSIFY_OPTIONS0, FWPM_CLASSIFY_OPTIONS0 structure [Network Drivers Starting with Windows Vista], FWPM_CLASSIFY_OPTIONS0_, fwpmtypes/FWPM_CLASSIFY_OPTIONS0, netvista.fwpm_classify_options0, wfp_ref_3_struct_2_fwpm_A-Z_382f5c3c-2eef-4841-b1ab-7fbb9254ee21.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
 - FWPM_CLASSIFY_OPTIONS0
product: Windows
targetos: Windows
req.typenames: FWPM_CLASSIFY_OPTIONS0
req.redist: 
---

# FWPM_CLASSIFY_OPTIONS0_ structure


## -description


The <b>FWPM_CLASSIFY_OPTIONS0</b> structure can be used to define multiple time-out options and data for use
  with the 
  <a href="https://msdn.microsoft.com/8653fac0-8b2f-4e77-9588-2854ae168c1a">FwpsClassifyOptionSet0</a> function.
<div class="alert"><b>Note</b>  <b>FWPM_CLASSIFY_OPTIONS0</b> is a specific version of <b>FWPM_CLASSIFY_OPTIONS</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field numOptions

A value that specifies the number of time-out options being defined.


### -field options

A pointer to an array of 
     <a href="https://msdn.microsoft.com/2ffc121d-9b57-4935-9784-12447d2e0c46">FWPM_CLASSIFY_OPTION0</a> structures that
     specify the various options being defined.


## -see-also




<a href="https://msdn.microsoft.com/2ffc121d-9b57-4935-9784-12447d2e0c46">FWPM_CLASSIFY_OPTION0</a>



<a href="https://msdn.microsoft.com/8653fac0-8b2f-4e77-9588-2854ae168c1a">FwpsClassifyOptionSet0</a>
 

 

