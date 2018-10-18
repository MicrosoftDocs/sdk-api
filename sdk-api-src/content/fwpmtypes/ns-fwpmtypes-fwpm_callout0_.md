---
UID: NS:fwpmtypes.FWPM_CALLOUT0_
title: FWPM_CALLOUT0_
author: windows-sdk-content
description: The FWPM_CALLOUT0 structure defines the data that is required for a callout driver to add a callout to the filter engine.Note  FWPM_CALLOUT0 is a specific version of FWPM_CALLOUT.
old-location: netvista\fwpm_callout0.htm
tech.root: NetVista
ms.assetid: a6f19d6d-4fce-4774-86c1-10d1bf77315f
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWPM_CALLOUT0, FWPM_CALLOUT0 structure [Network Drivers Starting with Windows Vista], FWPM_CALLOUT0_, fwpmtypes/FWPM_CALLOUT0, netvista.fwpm_callout0, wfp_ref_3_struct_2_fwpm_A-Z_53d3ca0d-80eb-43d6-9272-892e14bb4000.xml
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
 - FWPM_CALLOUT0
product: Windows
targetos: Windows
req.typenames: FWPM_CALLOUT0
req.redist: 
---

# FWPM_CALLOUT0_ structure


## -description


The <b>FWPM_CALLOUT0</b> structure defines the data that is required for a callout driver to add a callout
  to the filter engine.
<div class="alert"><b>Note</b>  <b>FWPM_CALLOUT0</b> is a specific version of <b>FWPM_CALLOUT</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field calloutKey

A GUID that uniquely identifies the callout. This must be the same value as the GUID that is
     specified for the 
     <b>calloutKey</b> member of the 
     <a href="https://msdn.microsoft.com/df6e9980-6c9b-4d01-a1d5-e5242a3ebc66">FWPS_CALLOUT0</a> structure when the callout
     driver registers the callout with the filter engine.


### -field displayData

An 
     <a href="https://msdn.microsoft.com/dfd92824-feea-4f57-ba2f-b2d56dee48ad">FWPM_DISPLAY_DATA0</a> structure that
     specifies a name and description for the callout.


### -field flags

Flags that specify callout-specific parameters. Possible flags are:
     





#### FWPM_CALLOUT_FLAG_PERSISTENT

This flag indicates that the callout is to be persistent across system reboots. A persistent
       callout can be referenced by boot-time and persistent filters.



#### FWPM_CALLOUT_FLAG_REGISTERED

This flag indicates that an existing callout is registered. For more information on registering
       callouts, see 
       <a href="https://msdn.microsoft.com/1f003775-4b93-44cd-8c58-18e0e3fb5656">FwpsCalloutRegister0</a>. Do not set
       this flag when adding new callouts.



#### FWPM_CALLOUT_FLAG_USES_PROVIDER_CONTEXT

This flag indicates that the callout uses the provider context from the corresponding 
       <a href="https://msdn.microsoft.com/cf5e3372-466e-44f0-8312-78318c5efb13">FWPS_FILTER0</a> filter structure.


### -field providerKey

A pointer to a GUID that identifies the provider with which the callout that is being added to the
     filter engine is associated. If the callout is not associated with a particular provider, a callout
     driver should set this member to <b>NULL</b>. For more information about providers, see the Windows Filtering
     Platform section in the Microsoft Windows SDK documentation.


### -field providerData

A 
     <a href="https://msdn.microsoft.com/dd0e5743-e261-4a53-b496-ac577d63b69f">FWP_BYTE_BLOB</a> structure that describes any
     provider-specific data that is associated with the callout. If the callout is not associated with a
     particular provider or if the provider does not associate any provider-specific data with callouts, a
     callout driver should set the 
     <b>Size</b> member of this structure to zero and the 
     <b>Data</b> member of this structure to <b>NULL</b>.


### -field applicableLayer

The management identifier for the filtering layer at which the callout is applicable. For more
     information, see 
     <a href="netvista.management_filtering_layer_identifiers">Management Filtering Layer
     Identifiers</a>.


### -field calloutId

This member is not used when a callout driver uses the FWPM_CALLOUT0 structure to add a callout to
     the filter engine.
     

If a callout driver retrieves an FWPM_CALLOUT0 structure from the filter engine, this member contains
     the run-time identifier for the callout.


## -remarks



A callout driver passes a pointer to an initialized FWPM_CALLOUT0 structure to the 
    <a href="https://msdn.microsoft.com/f88a31c4-f42c-487d-b6d8-f8f609f2faff">FwpmCalloutAdd0</a> function when adding a
    callout to the filter engine.

Callout drivers do not typically add their callouts to the filter engine. In most situations this is
    handled by a user-mode Windows Filtering Platform management application.




## -see-also




<a href="https://msdn.microsoft.com/dfd92824-feea-4f57-ba2f-b2d56dee48ad">FWPM_DISPLAY_DATA0</a>



<a href="https://msdn.microsoft.com/df6e9980-6c9b-4d01-a1d5-e5242a3ebc66">FWPS_CALLOUT0</a>



<a href="https://msdn.microsoft.com/cf5e3372-466e-44f0-8312-78318c5efb13">FWPS_FILTER0</a>



<a href="https://msdn.microsoft.com/dd0e5743-e261-4a53-b496-ac577d63b69f">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/f88a31c4-f42c-487d-b6d8-f8f609f2faff">FwpmCalloutAdd0</a>



<a href="https://msdn.microsoft.com/1f003775-4b93-44cd-8c58-18e0e3fb5656">FwpsCalloutRegister0</a>
 

 

