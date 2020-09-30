---
UID: NS:fwpstypes.FWPS_ACTION0_
title: FWPS_ACTION0 (fwpstypes.h)
description: The FWPS_ACTION0 structure specifies the run-time action that the filter engine takes if all of the filter's filtering conditions are true.Note  FWPS_ACTION0 is a specific version of FWPS_ACTION.
helpviewer_keywords: ["FWPS_ACTION0","FWPS_ACTION0 structure [Network Drivers Starting with Windows Vista]","fwpstypes/FWPS_ACTION0","netvista.fwps_action0","wfp_ref_3_struct_3_fwps_A-E_2621dcb1-3b0a-4e5a-8869-4d8b9f635f99.xml"]
old-location: netvista\fwps_action0.htm
tech.root: NetVista
ms.assetid: 1b192efc-e685-48bf-bf61-1419ce03a77a
ms.date: 12/05/2018
ms.keywords: FWPS_ACTION0, FWPS_ACTION0 structure [Network Drivers Starting with Windows Vista], fwpstypes/FWPS_ACTION0, netvista.fwps_action0, wfp_ref_3_struct_3_fwps_A-E_2621dcb1-3b0a-4e5a-8869-4d8b9f635f99.xml
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
targetos: Windows
req.typenames: FWPS_ACTION0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPS_ACTION0_
 - fwpstypes/FWPS_ACTION0_
 - FWPS_ACTION0
 - fwpstypes/FWPS_ACTION0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - fwpstypes.h
api_name:
 - FWPS_ACTION0
---

# FWPS_ACTION0 structure


## -description

The <b>FWPS_ACTION0</b> structure specifies the run-time action that the filter engine takes if all of
  the filter's filtering conditions are true.
<div class="alert"><b>Note</b>  <b>FWPS_ACTION0</b> is a specific version of <b>FWPS_ACTION</b>. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields

### -field type

An <b>FWP_ACTION_TYPE</b> value that represents the action that the filter engine takes if all of
     the filter's filtering conditions are true. For a filter that is passed to a callout's 
     <a href="/windows-hardware/drivers/ddi/content/_netvista/">notifyFn</a> or 
     <a href="/windows-hardware/drivers/ddi/content/_netvista/">classifyFn</a> callout function, this member will
     be one of the following values:
     





#### FWP_ACTION_CALLOUT_TERMINATING

Specifies that the callout driver's 
       <a href="/windows-hardware/drivers/ddi/content/_netvista/">classifyFn</a> callout function must return one
       of the following values for the action to be taken on the data:
       





##### FWP_ACTION_BLOCK

Block the data from being transmitted or received.



##### FWP_ACTION_PERMIT

Permit the data to be transmitted or received.

If the callout driver's 
       <a href="/windows-hardware/drivers/ddi/content/_netvista/">classifyFn</a> callout function returns any
       other value for the action to be taken on the data, it is handled the same as if the callout driver's 
       classifyFn callout function returned
       <b>FWP_ACTION_BLOCK</b>.



#### FWP_ACTION_CALLOUT_INSPECTION

Specifies that the callout driver's 
       <a href="/windows-hardware/drivers/ddi/content/_netvista/">classifyFn</a> callout function must return the
       following value for the action to be taken on the data.
       





##### FWP_ACTION_CONTINUE

Continue on to the next filter.

If the callout driver's 
       <a href="/windows-hardware/drivers/ddi/content/_netvista/">classifyFn</a> callout function returns any
       other value for the action to be taken on the data, it is handled the same as if the callout driver's 
       classifyFn callout function returned
       <b>FWP_ACTION_CONTINUE</b>.



#### FWP_ACTION_CALLOUT_UNKNOWN

Specifies that the callout driver's 
       <a href="/windows-hardware/drivers/ddi/content/_netvista/">classifyFn</a> callout function can return any
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
     <a href="/windows-hardware/drivers/ddi/content/fwpsk/nf-fwpsk-fwpscalloutregister0">FwpsCalloutRegister0</a> function to
     register the callout with the filter engine.

## -remarks

An FWPS_ACTION0 structure is contained within an 
    [FWPS_FILTER0](/windows/desktop/api/fwpstypes/ns-fwpstypes-fwps_filter0) structure.

## -see-also

[FWPS_FILTER0](/windows/desktop/api/fwpstypes/ns-fwpstypes-fwps_filter0)



<a href="/windows-hardware/drivers/ddi/content/fwpsk/nf-fwpsk-fwpscalloutregister0">FwpsCalloutRegister0</a>



<a href="/windows-hardware/drivers/network/types-of-callouts">Types of Callouts</a>



<a href="/windows-hardware/drivers/ddi/content/_netvista/">classifyFn</a>



<a href="/windows-hardware/drivers/ddi/content/_netvista/">notifyFn</a>