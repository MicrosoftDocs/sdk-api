---
UID: NS:fwpstypes.FWPS_ACTION0_
title: FWPS_ACTION0_
author: windows-sdk-content
description: The FWPS_ACTION0 structure specifies the run-time action that the filter engine takes if all of the filter's filtering conditions are true.Note  FWPS_ACTION0 is a specific version of FWPS_ACTION.
old-location: netvista\fwps_action0.htm
tech.root: NetVista
ms.assetid: 1b192efc-e685-48bf-bf61-1419ce03a77a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWPS_ACTION0, FWPS_ACTION0 structure [Network Drivers Starting with Windows Vista], FWPS_ACTION0_, fwpstypes/FWPS_ACTION0, netvista.fwps_action0, wfp_ref_3_struct_3_fwps_A-E_2621dcb1-3b0a-4e5a-8869-4d8b9f635f99.xml
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - FWPS_ACTION0
product: Windows
targetos: Windows
req.typenames: FWPS_ACTION0
req.redist: 
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
     <a href="https://msdn.microsoft.com/48b4965a-7284-4331-a900-0e3a2a1a0bc9">notifyFn</a> or 
     <a href="https://msdn.microsoft.com/3753daab-a08d-42ce-a284-07538ac538df">classifyFn</a> callout function, this member will
     be one of the following values:
     





#### FWP_ACTION_CALLOUT_TERMINATING

Specifies that the callout driver's 
       <a href="https://msdn.microsoft.com/3753daab-a08d-42ce-a284-07538ac538df">classifyFn</a> callout function must return one
       of the following values for the action to be taken on the data:
       





##### FWP_ACTION_BLOCK

Block the data from being transmitted or received.



##### FWP_ACTION_PERMIT

Permit the data to be transmitted or received.

If the callout driver's 
       <a href="https://msdn.microsoft.com/3753daab-a08d-42ce-a284-07538ac538df">classifyFn</a> callout function returns any
       other value for the action to be taken on the data, it is handled the same as if the callout driver's 
       classifyFn callout function returned
       <b>FWP_ACTION_BLOCK</b>.



#### FWP_ACTION_CALLOUT_INSPECTION

Specifies that the callout driver's 
       <a href="https://msdn.microsoft.com/3753daab-a08d-42ce-a284-07538ac538df">classifyFn</a> callout function must return the
       following value for the action to be taken on the data.
       





##### FWP_ACTION_CONTINUE

Continue on to the next filter.

If the callout driver's 
       <a href="https://msdn.microsoft.com/3753daab-a08d-42ce-a284-07538ac538df">classifyFn</a> callout function returns any
       other value for the action to be taken on the data, it is handled the same as if the callout driver's 
       classifyFn callout function returned
       <b>FWP_ACTION_CONTINUE</b>.



#### FWP_ACTION_CALLOUT_UNKNOWN

Specifies that the callout driver's 
       <a href="https://msdn.microsoft.com/3753daab-a08d-42ce-a284-07538ac538df">classifyFn</a> callout function can return any
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
     <a href="https://msdn.microsoft.com/1f003775-4b93-44cd-8c58-18e0e3fb5656">FwpsCalloutRegister0</a> function to
     register the callout with the filter engine.


## -remarks



An FWPS_ACTION0 structure is contained within an 
    <a href="https://msdn.microsoft.com/cf5e3372-466e-44f0-8312-78318c5efb13">FWPS_FILTER0</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/cf5e3372-466e-44f0-8312-78318c5efb13">FWPS_FILTER0</a>



<a href="https://msdn.microsoft.com/1f003775-4b93-44cd-8c58-18e0e3fb5656">FwpsCalloutRegister0</a>



<a href="netvista.types_of_callouts">Types of Callouts</a>



<a href="https://msdn.microsoft.com/3753daab-a08d-42ce-a284-07538ac538df">classifyFn</a>



<a href="https://msdn.microsoft.com/48b4965a-7284-4331-a900-0e3a2a1a0bc9">notifyFn</a>
 

 

