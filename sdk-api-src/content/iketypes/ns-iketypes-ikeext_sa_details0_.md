---
UID: NS:iketypes.IKEEXT_SA_DETAILS0_
title: IKEEXT_SA_DETAILS0_
author: windows-driver-content
description: Is used to store information returned when enumerating IKE, AuthIP, or IKEv2 security associations (SAs).
old-location: fwp\ikeext_sa_details0.htm
old-project: FWP
ms.assetid: 63d33420-9ae5-4b82-a5f9-469cc5652d59
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IKEEXT_SA_DETAILS0, IKEEXT_SA_DETAILS0 structure [Filtering], IKEEXT_SA_DETAILS0_, fwp.ikeext_sa_details0, iketypes/IKEEXT_SA_DETAILS0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IKEEXT_SA_DETAILS0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iketypes.h
api_name:
-	IKEEXT_SA_DETAILS0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKEEXT_SA_DETAILS0_ structure


## -description


The <b>IKEEXT_SA_DETAILS0</b> structure is used to store information returned when enumerating IKE, AuthIP, or IKEv2 security associations (SAs).
<div class="alert"><b>Note</b>  <b>IKEEXT_SA_DETAILS0</b> is the specific implementation of IKEEXT_SA_DETAILS used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/b4b8767b-399a-49f0-91fd-59c2206742de">IKEEXT_SA_DETAILS1</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/51b8f3a8-bccc-4d1f-871f-9a319ed5c49c">IKEEXT_SA_DETAILS2</a> is available. </div><div> </div>

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

Credentials information for the SA specified by <a href="https://msdn.microsoft.com/048d0a56-5d9b-4a85-b42f-8505eb6a97a9">IKEEXT_CREDENTIALS0</a>.


### -field ikePolicyKey

GUID of the main mode policy provider context corresponding to this SA.


### -field virtualIfTunnelId

ID/Handle to virtual interface tunneling state.

Applicable only to IKEv2.

Available only on Windows 7, Windows Server 2008 R2, and later.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

