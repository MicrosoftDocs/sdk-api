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

# IKEEXT_SA_DETAILS1_ structure


## -description


The <b>IKEEXT_SA_DETAILS1</b> structure is used to store information returned when enumerating IKE, AuthIP, and IKEv2 security associations (SAs).
<div class="alert"><b>Note</b>  <b>IKEEXT_SA_DETAILS1</b> is the specific implementation of IKEEXT_SA_DETAILS used in Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/51b8f3a8-bccc-4d1f-871f-9a319ed5c49c">IKEEXT_SA_DETAILS2</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/63d33420-9ae5-4b82-a5f9-469cc5652d59">IKEEXT_SA_DETAILS0</a> is available.</div><div> </div>

## -struct-fields




### -field saId

LUID identifying the security association.


### -field keyModuleType

Key module type. 

See <a href="https://msdn.microsoft.com/a9268b07-343a-4a51-bc70-3e624facf617">IKEEXT_KEY_MODULE_TYPE</a> for more information. 


### -field ipVersion

IP version specified by <a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a>.


### -field v4UdpEncapsulation

Points to an  <a href="https://msdn.microsoft.com/69cddec0-7311-4833-8b24-293ad714054e">IPSEC_V4_UDP_ENCAPSULATION0</a> structure, which, if a NAT is detected,  stores the UDP ports corresponding to the 
   Main Mode.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>. 


### -field ikeTraffic

The traffic corresponding to this IKE SA specified by <a href="https://msdn.microsoft.com/99cb3774-7afd-44fd-9c3e-e2d913aaeecb">IKEEXT_TRAFFIC0</a>.


### -field ikeProposal

The main mode proposal corresponding to this IKE SA specified by <a href="https://msdn.microsoft.com/59568ef7-12bd-407a-a8ee-9bf261f49883">IKEEXT_PROPOSAL0</a>.


### -field cookiePair

SA cookies specified by <a href="https://msdn.microsoft.com/c752545b-1880-40ac-871e-e36d4b81668f">IKEEXT_COOKIE_PAIR0</a>.


### -field ikeCredentials

Credentials information for the SA specified by <a href="https://msdn.microsoft.com/dbd895bd-a720-4c8e-a2e7-f5614d69922c">IKEEXT_CREDENTIALS1</a>.


### -field ikePolicyKey

GUID of the main mode policy provider context corresponding to this SA.


### -field virtualIfTunnelId

ID/Handle to virtual interface tunneling state. Applicable only to IKEv2.


### -field correlationKey

 




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

