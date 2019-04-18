---
UID: NS:fwpmtypes.FWPM_NET_EVENT3_
title: FWPM_NET_EVENT3 (fwpmtypes.h)
author: windows-sdk-content
description: Contains information about all event types.
old-location: fwp\fwpm_net_event3.htm
tech.root: fwp
ms.assetid: 2D71C44C-B553-46DD-8943-DCC979A7DC6B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT3, FWPM_NET_EVENT3 structure [Filtering], fwp.fwpm_net_event3, fwpmtypes/FWPM_NET_EVENT3
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
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
 - Fwpmtypes.h
api_name:
 - FWPM_NET_EVENT3
product: Windows
targetos: Windows
req.typenames: FWPM_NET_EVENT3
req.redist: 
ms.custom: 19H1
---

# FWPM_NET_EVENT3 structure


## -description


The <b>FWPM_NET_EVENT3</b> structure contains information about all event types.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT3</b> is the specific implementation of FWPM_NET_EVENT used in Windows 10, version 1607. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information.  For  Windows 8, <a href="https://msdn.microsoft.com/fbcacfb1-b471-474e-bdee-12a481fadc63">FWPM_NET_EVENT2</a> is available. For Windows 7, <a href="https://msdn.microsoft.com/0f989f66-8373-4546-ade3-8b337c4507e2">FWPM_NET_EVENT1</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/91e15135-49b8-497e-8f09-984e9af64dbe">FWPM_NET_EVENT0</a> is available.</div><div> </div>

## -struct-fields




### -field header

Information common to all events.


### -field type

The type of event.


### -field ikeMmFailure

Information about  an IKE main mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE</b>.


### -field ikeQmFailure

Information about  an IKE quick mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE</b>.


### -field ikeEmFailure

Information about  an IKE user mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE</b>.


### -field classifyDrop

Information about  a drop event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_CLASSIFY_DROP</b>.


### -field ipsecDrop

Information about an IPsec kernel drop event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP</b>.


### -field idpDrop

Information about an IPsec DoS Protection event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_IPSEC_DOSP_DROP</b>.


### -field classifyAllow

Information about an allow event.


### -field capabilityDrop

Information about a capability-related drop event.


### -field capabilityAllow

Information about a capability-related allow event.


### -field classifyDropMac

Information about a MAC layer drop event.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

