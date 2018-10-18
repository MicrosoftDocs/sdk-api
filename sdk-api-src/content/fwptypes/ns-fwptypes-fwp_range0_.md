---
UID: NS:fwptypes.FWP_RANGE0_
title: FWP_RANGE0_
author: windows-sdk-content
description: The FWP_RANGE0 structure defines a range of values.Note  FWP_RANGE0 is a specific version of FWP_RANGE.
old-location: netvista\fwp_range0.htm
tech.root: NetVista
ms.assetid: 66410df3-0856-4b2e-a586-1a75b97e0047
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWP_RANGE0, FWP_RANGE0 structure [Network Drivers Starting with Windows Vista], FWP_RANGE0_, fwptypes/FWP_RANGE0, netvista.fwp_range0, wfp_ref_3_struct_1_top_fwp_A-Z_3f37ba0a-8d01-4319-a592-3ac052dd81e6.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: fwptypes.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwptypes.h
api_name:
 - FWP_RANGE0
product: Windows
targetos: Windows
req.typenames: FWP_RANGE0
req.redist: 
---

# FWP_RANGE0_ structure


## -description


The <b>FWP_RANGE0</b> structure defines a range of values.
<div class="alert"><b>Note</b>  <b>FWP_RANGE0</b> is a specific version of <b>FWP_RANGE</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field valueLow

An 
     <a href="https://msdn.microsoft.com/0d8557cd-bd11-4786-ba6e-fbbeb2e2b761">FWP_VALUE0</a> structure that specifies the
     beginning value in the range of values. This value is included in the range.


### -field valueHigh

An 
     <a href="https://msdn.microsoft.com/0d8557cd-bd11-4786-ba6e-fbbeb2e2b761">FWP_VALUE0</a> structure that specifies the ending
     value in the range of values. This value is included in the range.


## -remarks



The FWP_RANGE0 structure specifies a range of values that data can be tested against for a filtering
    condition.

The type of value specified in the 
    <a href="https://msdn.microsoft.com/0d8557cd-bd11-4786-ba6e-fbbeb2e2b761">FWP_VALUE0</a> structures must be identical for both
    the 
    <b>valueLow</b> and 
    <b>valueHigh</b> members.

The numeric value of the 
    <b>valueHigh</b> member must be greater than or equal to the numeric value of the 
    <b>valueLow</b> member.




## -see-also




<a href="https://msdn.microsoft.com/8d0aad8c-b224-4066-a10a-7c11ca60a78c">FWP_CONDITION_VALUE0</a>



<a href="https://msdn.microsoft.com/7632d9be-dd16-40d2-b7b4-2d4efb6aaa99">FWP_DATA_TYPE</a>



<a href="https://msdn.microsoft.com/0d8557cd-bd11-4786-ba6e-fbbeb2e2b761">FWP_VALUE0</a>
 

 

