---
UID: NS:fwpstypes.FWPS_INCOMING_VALUE0_
title: FWPS_INCOMING_VALUE0_
author: windows-sdk-content
description: The FWPS_INCOMING_VALUE0 structure defines an individual data value.Note  FWPS_INCOMING_VALUE0 is a specific version of FWPS_INCOMING_VALUE.
old-location: netvista\fwps_incoming_value0.htm
old-project: netvista
ms.assetid: 94a81a93-7c92-4c0a-9ac7-c2085175c1a7
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: FWPS_INCOMING_VALUE0, FWPS_INCOMING_VALUE0 structure [Network Drivers Starting with Windows Vista], FWPS_INCOMING_VALUE0_, fwpstypes/FWPS_INCOMING_VALUE0, netvista.fwps_incoming_value0, wfp_ref_3_struct_3_fwps_F-O_de0ecafa-7ade-4473-a04e-3fb924c22db0.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwpstypes.h
req.include-header: Fwpsk.h
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
req.typenames: FWPS_INCOMING_VALUE0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	fwpstypes.h
api_name:
-	FWPS_INCOMING_VALUE0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# FWPS_INCOMING_VALUE0_ structure


## -description


The <b>FWPS_INCOMING_VALUE0</b> structure defines an individual data value.
<div class="alert"><b>Note</b>  <b>FWPS_INCOMING_VALUE0</b> is a specific version of <b>FWPS_INCOMING_VALUE</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field value

An 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a> structure that contains the data value.


## -remarks



The 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff552401">FWPS_INCOMING_VALUES0</a> structure
    contains a pointer to an array of FWPS_INCOMING_VALUE0 structures that contain the incoming data values
    that are passed to a callout's 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552401">FWPS_INCOMING_VALUES0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552450">FWP_VALUE0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a>
 

 

