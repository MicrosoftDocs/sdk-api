---
UID: NS:fwpmtypes.FWPM_SESSION0_
title: FWPM_SESSION0_
author: windows-sdk-content
description: The FWPM_SESSION0 structure defines session-specific parameters for an open session to the filter engine.Note  FWPM_SESSION0 is a specific version of FWPM_SESSION.
old-location: netvista\fwpm_session0.htm
tech.root: NetVista
ms.assetid: 971faf9c-2847-4829-ae96-b9fde15f5c26
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FWPM_SESSION0, FWPM_SESSION0 structure [Network Drivers Starting with Windows Vista], FWPM_SESSION0_, fwpmtypes/FWPM_SESSION0, netvista.fwpm_session0, wfp_ref_3_struct_2_fwpm_A-Z_29684a7b-29ea-42b3-9351-d7d847ef4717.xml
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
 - FWPM_SESSION0
product: Windows
targetos: Windows
req.typenames: FWPM_SESSION0
req.redist: 
---

# FWPM_SESSION0_ structure


## -description


The <b>FWPM_SESSION0</b> structure defines session-specific parameters for an open session to the filter
  engine.
<div class="alert"><b>Note</b>  <b>FWPM_SESSION0</b> is a specific version of <b>FWPM_SESSION</b>. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.</div><div> </div>

## -struct-fields




### -field sessionKey

A callout driver-defined GUID that uniquely identifies the open session to the filter engine. If a
     callout driver zero-initializes this GUID prior to opening the session, the filter engine will generate
     a unique GUID when the session is opened.


### -field displayData

An 
     <a href="https://msdn.microsoft.com/dfd92824-feea-4f57-ba2f-b2d56dee48ad">FWPM_DISPLAY_DATA0</a> structure that
     specifies a name and a description for the open session to the filter engine.


### -field flags

Flags that specify the session-specific parameters. Possible flags are:
     





#### FWPM_SESSION_FLAG_DYNAMIC

If this flag is set, any filters, providers, provider contexts, or callouts that are added to
       the filter engine during the open session will be automatically removed from the filter engine when
       the session is closed. No filters, providers, provider contexts, or callouts can be deleted during the
       open session except for those that are added during the session.


### -field txnWaitTimeoutInMSec

The time, in milliseconds, that the callout driver will wait to begin a transaction with the
     filter engine before a time-out occurs. If a callout driver specifies zero for this member, a default
     time-out value will be used.


### -field processId

This member is not used when a callout driver specifies an <b>FWPM_SESSION0</b> structure when opening a
     session to the filter engine.


### -field sid

This member is not used when a callout driver specifies an <b>FWPM_SESSION0</b> structure when opening a
     session to the filter engine.


### -field username

This member is not used when a callout driver specifies an <b>FWPM_SESSION0</b> structure when opening a
     session to the filter engine.


### -field kernelMode

This member is not used when a callout driver specifies an <b>FWPM_SESSION0</b> structure when opening a
     session to the filter engine.


## -remarks



A callout driver can pass a pointer to an <b>FWPM_SESSION0</b> structure to the 
    <a href="https://msdn.microsoft.com/4d805ffe-7cf9-4cbc-9077-e191ddc24ecd">FwpmEngineOpen0</a> function to specify
    session-specific parameters for the session to the filter engine.




## -see-also




<a href="https://msdn.microsoft.com/dfd92824-feea-4f57-ba2f-b2d56dee48ad">FWPM_DISPLAY_DATA0</a>



<a href="https://msdn.microsoft.com/4d805ffe-7cf9-4cbc-9077-e191ddc24ecd">FwpmEngineOpen0</a>
 

 

