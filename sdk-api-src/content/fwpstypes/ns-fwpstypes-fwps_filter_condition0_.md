---
UID: NS:fwpstypes.FWPS_FILTER_CONDITION0_
title: FWPS_FILTER_CONDITION0_
author: windows-sdk-content
description: The FWPS_FILTER_CONDITION0 structure defines a run-time filtering condition for a filter.Note  FWPS_FILTER_CONDITION0 is a specific version of FWPS_FILTER_CONDITION.
old-location: netvista\fwps_filter_condition0.htm
tech.root: netvista
ms.assetid: d4a20939-4866-4402-9b29-d94c2170807c
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: FWPS_FILTER_CONDITION0, FWPS_FILTER_CONDITION0 structure [Network Drivers Starting with Windows Vista], FWPS_FILTER_CONDITION0_, fwpstypes/FWPS_FILTER_CONDITION0, netvista.fwps_filter_condition0, wfp_ref_3_struct_3_fwps_F-O_93287819-7faf-41d5-a128-946293c1eb73.xml
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpstypes.h
api_name:
 - FWPS_FILTER_CONDITION0
product: Windows
targetos: Windows
req.typenames: FWPS_FILTER_CONDITION0
req.redist: 
---

# FWPS_FILTER_CONDITION0_ structure


## -description


The <b>FWPS_FILTER_CONDITION0</b> structure defines a run-time filtering condition for a filter.
<div class="alert"><b>Note</b>  <b>FWPS_FILTER_CONDITION0</b> is a specific version of <b>FWPS_FILTER_CONDITION</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field fieldId

The data field identifier for the data field tested by this filtering condition. The meaning of
     the numeric value of this member is specific to the filtering layer specified by the 
     <b>layerId</b> member. For a description of the data field identifiers for each filtering layer, see 
     <a href="https://msdn.microsoft.com/6e617ef4-807b-4564-8b95-b289edfee8d2">Data Field Identifiers</a>.


### -field reserved

Reserved for system use. Callout drivers should ignore this member.


### -field matchType

An 
     <a href="https://msdn.microsoft.com/c0f95b3f-1b89-4d44-87b2-73032fa3524e">FWP_MATCH_TYPE</a> value that specifies the type
     of match that the filter engine is to test on the data field to check whether the filtering condition is
     true.


### -field conditionValue

An 
     <a href="https://msdn.microsoft.com/8d0aad8c-b224-4066-a10a-7c11ca60a78c">FWP_CONDITION_VALUE0</a> structure that
     specifies the value against which the data field is tested.


## -remarks



The 
    <b>filterCondition</b> member of the 
    <a href="https://msdn.microsoft.com/cf5e3372-466e-44f0-8312-78318c5efb13">FWPS_FILTER0</a> structure points to an array of
    FWPS_FILTER_CONDITION0 structures that specify the run-time filtering conditions for a filter.




## -see-also




<a href="https://msdn.microsoft.com/cf5e3372-466e-44f0-8312-78318c5efb13">FWPS_FILTER0</a>



<a href="https://msdn.microsoft.com/8d0aad8c-b224-4066-a10a-7c11ca60a78c">FWP_CONDITION_VALUE0</a>



<a href="https://msdn.microsoft.com/c0f95b3f-1b89-4d44-87b2-73032fa3524e">FWP_MATCH_TYPE</a>
 

 

