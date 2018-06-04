---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff546312">Data Field Identifiers</a>.


### -field reserved

Reserved for system use. Callout drivers should ignore this member.


### -field matchType

An 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552437">FWP_MATCH_TYPE</a> value that specifies the type
     of match that the filter engine is to test on the data field to check whether the filtering condition is
     true.


### -field conditionValue

An 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a> structure that
     specifies the value against which the data field is tested.


## -remarks



The 
    <b>filterCondition</b> member of the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff552387">FWPS_FILTER0</a> structure points to an array of
    FWPS_FILTER_CONDITION0 structures that specify the run-time filtering conditions for a filter.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552387">FWPS_FILTER0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552430">FWP_CONDITION_VALUE0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552437">FWP_MATCH_TYPE</a>
 

 

