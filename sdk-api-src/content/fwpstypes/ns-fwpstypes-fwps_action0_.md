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

# FWPS_ACTION0_ structure


## -description


The <b>FWPS_ACTION0</b> structure specifies the run-time action that the filter engine takes if all of
  the filter's filtering conditions are true.
<div class="alert"><b>Note</b>  <b>FWPS_ACTION0</b> is a specific version of <b>FWPS_ACTION</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field type

An <b>FWP_ACTION_TYPE</b> value that represents the action that the filter engine takes if all of
     the filter's filtering conditions are true. For a filter that is passed to a callout's 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff568802">notifyFn</a> or 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function, this member will
     be one of the following values:
     





#### FWP_ACTION_CALLOUT_TERMINATING

Specifies that the callout driver's 
       <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function must return one
       of the following values for the action to be taken on the data:
       





##### FWP_ACTION_BLOCK

Block the data from being transmitted or received.



##### FWP_ACTION_PERMIT

Permit the data to be transmitted or received.

If the callout driver's 
       <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function returns any
       other value for the action to be taken on the data, it is handled the same as if the callout driver's 
       classifyFn callout function returned
       <b>FWP_ACTION_BLOCK</b>.



#### FWP_ACTION_CALLOUT_INSPECTION

Specifies that the callout driver's 
       <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function must return the
       following value for the action to be taken on the data.
       





##### FWP_ACTION_CONTINUE

Continue on to the next filter.

If the callout driver's 
       <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function returns any
       other value for the action to be taken on the data, it is handled the same as if the callout driver's 
       classifyFn callout function returned
       <b>FWP_ACTION_CONTINUE</b>.



#### FWP_ACTION_CALLOUT_UNKNOWN

Specifies that the callout driver's 
       <a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a> callout function can return any
       of the following values for the action to be taken on the data:
       





##### FWP_ACTION_BLOCK

Block the data from being transmitted or received.



##### FWP_ACTION_PERMIT

Permit the data to be transmitted or received.



##### FWP_ACTION_CONTINUE

Continue on to the next filter.


### -field calloutId

The run-time identifier for the callout that the filter engine calls if all of the filter's
     filtering conditions are true. This is the same identifier that was returned when the callout driver
     called the 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff551140">FwpsCalloutRegister0</a> function to
     register the callout with the filter engine.


## -remarks



An FWPS_ACTION0 structure is contained within an 
    <a href="https://msdn.microsoft.com/library/windows/hardware/ff552387">FWPS_FILTER0</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552387">FWPS_FILTER0</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551140">FwpsCalloutRegister0</a>



<a href="netvista.types_of_callouts">Types of Callouts</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff544887">classifyFn</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff568802">notifyFn</a>
 

 

