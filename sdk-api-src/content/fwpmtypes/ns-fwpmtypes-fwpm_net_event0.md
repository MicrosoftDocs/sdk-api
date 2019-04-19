---
UID: NS:fwpmtypes.FWPM_NET_EVENT0_
title: FWPM_NET_EVENT0 (fwpmtypes.h)
author: windows-sdk-content
description: Contains information about all event types.
old-location: fwp\fwpm_net_event0.htm
tech.root: fwp
ms.assetid: 91e15135-49b8-497e-8f09-984e9af64dbe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FWPM_NET_EVENT0, FWPM_NET_EVENT0 structure [Filtering], fwp.fwpm_net_event0, fwpmtypes/FWPM_NET_EVENT0
ms.topic: struct
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - FWPM_NET_EVENT0
product: Windows
targetos: Windows
req.typenames: FWPM_NET_EVENT0
req.redist: 
ms.custom: 19H1
---

# FWPM_NET_EVENT0 structure


## -description


The <b>FWPM_NET_EVENT0</b> structure contains information about all event types.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT0</b> is the specific implementation of FWPM_NET_EVENT used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/0f989f66-8373-4546-ade3-8b337c4507e2">FWPM_NET_EVENT1</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/fbcacfb1-b471-474e-bdee-12a481fadc63">FWPM_NET_EVENT2</a> is available.</div><div> </div>

## -struct-fields




### -field header

A <a href="https://msdn.microsoft.com/2fbb805d-d38b-4918-a291-fe1000ac2ea2">FWPM_NET_EVENT_HEADER0</a> structure that contains information common to all events.


### -field type

A <a href="https://msdn.microsoft.com/75dd3b0f-d809-421e-ac70-b8bf5d38757c">FWPM_NET_EVENT_TYPE</a> value that specifies the type of event.


### -field ikeMmFailure

Address of an <a href="https://msdn.microsoft.com/en-us/library/Aa364279(v=VS.85).aspx">FWPM_NET_EVENT_IKEEXT_MM_FAILURE0</a> structure that contains information about  an IKE main mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE</b>.


### -field ikeQmFailure

Address of an <a href="https://msdn.microsoft.com/en-us/library/Aa364280(v=VS.85).aspx">FWPM_NET_EVENT_IKEEXT_QM_FAILURE0</a> structure that contains information about  an IKE quick mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE</b>.


### -field ikeEmFailure

Address of an <a href="https://msdn.microsoft.com/en-us/library/Aa364278(v=VS.85).aspx">FWPM_NET_EVENT_IKEEXT_EM_FAILURE0</a> structure that contains information about  an IKE user mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE</b>.


### -field classifyDrop

Address of an <a href="https://msdn.microsoft.com/9688ff75-292f-44f2-b3ed-41a9dd1ef918">FWPM_NET_EVENT_CLASSIFY_DROP0</a> structure that contains information about  a drop event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_CLASSIFY_DROP</b>.


### -field ipsecDrop

Address of an <a href="https://msdn.microsoft.com/en-us/library/Aa814096(v=VS.85).aspx">FWPM_NET_EVENT_IPSEC_KERNEL_DROP0</a> structure that contains information about an IPsec kernel drop event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP</b>.


### -field idpDrop

Address of an <a href="https://msdn.microsoft.com/en-us/library/Dd744950(v=VS.85).aspx">FWPM_NET_EVENT_IPSEC_DOSP_DROP0</a> structure that contains information about an IPsec DoS Protection event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_IPSEC_DOSP_DROP</b>.

<div class="alert"><b>Note</b>  Available only in Windows Server 2008 R2, Windows 7, and later.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

