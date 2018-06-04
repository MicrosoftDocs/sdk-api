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

# FWPM_NET_EVENT2_ structure


## -description


The <b>FWPM_NET_EVENT2</b> structure contains information about all event types.
<div class="alert"><b>Note</b>  <b>FWPM_NET_EVENT2</b> is the specific implementation of FWPM_NET_EVENT used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/0f989f66-8373-4546-ade3-8b337c4507e2">FWPM_NET_EVENT1</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/91e15135-49b8-497e-8f09-984e9af64dbe">FWPM_NET_EVENT0</a> is available.</div><div> </div>

## -struct-fields




### -field header

Type: <b><a href="https://msdn.microsoft.com/1120d807-9188-4674-9acd-4b96e680f8af">FWPM_NET_EVENT_HEADER2</a></b>

Information common to all events.


### -field type

Type: <b><a href="https://msdn.microsoft.com/75dd3b0f-d809-421e-ac70-b8bf5d38757c">FWPM_NET_EVENT_TYPE</a></b>

The type of event.


### -field ikeMmFailure

Type: <b><a href="https://msdn.microsoft.com/4c67353c-289c-42ef-9081-20c33a9a06a4">FWPM_NET_EVENT_IKEEXT_MM_FAILURE1</a>*</b>

Information about  an IKE main mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_MM_FAILURE</b>.


### -field ikeQmFailure

Type: <b><a href="https://msdn.microsoft.com/a9cffcee-67a2-4a04-9ff1-85e2e02fa9a9">FWPM_NET_EVENT_IKEEXT_QM_FAILURE0</a>*</b>

Information about  an IKE quick mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_QM_FAILURE</b>.


### -field ikeEmFailure

Type: <b><a href="https://msdn.microsoft.com/42348e1d-e3b3-4f8c-9fef-15e2e4ebf580">FWPM_NET_EVENT_IKEEXT_EM_FAILURE1</a>*</b>

Information about  an IKE user mode failure.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IKEEXT_EM_FAILURE</b>.


### -field classifyDrop

Type: <b><a href="https://msdn.microsoft.com/1e018d6c-ed56-43f9-90b3-f2af42861617">FWPM_NET_EVENT_CLASSIFY_DROP2</a>*</b>

Information about  a drop event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_CLASSIFY_DROP</b>.


### -field ipsecDrop

Type: <b><a href="https://msdn.microsoft.com/ef970199-3603-4012-9033-afa4a7301fea">FWPM_NET_EVENT_IPSEC_KERNEL_DROP0</a>*</b>

Information about an IPsec kernel drop event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_TYPE_IPSEC_KERNEL_DROP</b>.


### -field idpDrop

Type: <b><a href="https://msdn.microsoft.com/7b28a81f-bf80-4739-989e-a276a0ca8a3a">FWPM_NET_EVENT_IPSEC_DOSP_DROP0</a>*</b>

Information about an IPsec DoS Protection event.

Available when <b>type</b> is <b>FWPM_NET_EVENT_IPSEC_DOSP_DROP</b>.


### -field classifyAllow

Type: <b><a href="https://msdn.microsoft.com/4c7b665e-b248-4506-8d5f-bd27b05d8d50">FWPM_NET_EVENT_CLASSIFY_ALLOW0</a>*</b>

Information about an allow event.


### -field capabilityDrop

Type: <b><a href="https://msdn.microsoft.com/40848332-0961-417c-8adc-dd1a380594ba">FWPM_NET_EVENT_CAPABILITY_DROP0</a>*</b>

Information about a capability-related drop event.


### -field capabilityAllow

Type: <b><a href="https://msdn.microsoft.com/e53e92e5-f7fa-4457-8681-754b50b24273">FWPM_NET_EVENT_CAPABILITY_ALLOW0</a>*</b>

Information about a capability-related allow event.


### -field classifyDropMac

Type: <b><a href="https://msdn.microsoft.com/750c2cfa-6799-492d-9e10-b4260541ada7">FWPM_NET_EVENT_CLASSIFY_DROP_MAC0</a>*</b>

Information about a MAC layer drop event.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

