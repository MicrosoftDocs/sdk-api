---
UID: NS:iketypes.IKEEXT_SA_DETAILS2_
title: IKEEXT_SA_DETAILS2_
author: windows-driver-content
description: Is used to store information returned when enumerating IKE, AuthIP, and IKEv2 security associations (SAs).
old-location: fwp\ikeext_sa_details2.htm
old-project: FWP
ms.assetid: 51b8f3a8-bccc-4d1f-871f-9a319ed5c49c
ms.author: windowsdriverdev
ms.date: 4/12/2018
ms.keywords: IKEEXT_SA_DETAILS2, IKEEXT_SA_DETAILS2 structure [Filtering], IKEEXT_SA_DETAILS2_, fwp.ikeext_sa_details2, iketypes/IKEEXT_SA_DETAILS2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IKEEXT_SA_DETAILS2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	iketypes.h
api_name:
-	IKEEXT_SA_DETAILS2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKEEXT_SA_DETAILS2_ structure


## -description


The <b>IKEEXT_SA_DETAILS2</b> structure is used to store information returned when enumerating IKE, AuthIP, and IKEv2 security associations (SAs).
<div class="alert"><b>Note</b>  <b>IKEEXT_SA_DETAILS2</b> is the specific implementation of IKEEXT_SA_DETAILS used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/b4b8767b-399a-49f0-91fd-59c2206742de">IKEEXT_SA_DETAILS1</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/63d33420-9ae5-4b82-a5f9-469cc5652d59">IKEEXT_SA_DETAILS0</a>  is available.</div><div> </div>

## -struct-fields




### -field saId

Type: <b>UINT64</b>

LUID identifying the security association.


### -field keyModuleType

Type: <b><a href="https://msdn.microsoft.com/a9268b07-343a-4a51-bc70-3e624facf617">IKEEXT_KEY_MODULE_TYPE</a></b>

Key module type. 


### -field ipVersion

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a></b>

 The IP version.


### -field v4UdpEncapsulation

Type: <b><a href="https://msdn.microsoft.com/69cddec0-7311-4833-8b24-293ad714054e">IPSEC_V4_UDP_ENCAPSULATION0</a>*</b>

Stores the UDP ports corresponding to the 
   Main Mode, if a NAT is detected.

Available when <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>. 


### -field ikeTraffic

Type: <b><a href="https://msdn.microsoft.com/99cb3774-7afd-44fd-9c3e-e2d913aaeecb">IKEEXT_TRAFFIC0</a></b>

The traffic corresponding to this IKE SA.


### -field ikeProposal

Type: <b><a href="https://msdn.microsoft.com/59568ef7-12bd-407a-a8ee-9bf261f49883">IKEEXT_PROPOSAL0</a></b>

The main mode proposal corresponding to this IKE SA.


### -field cookiePair

Type: <b><a href="https://msdn.microsoft.com/c752545b-1880-40ac-871e-e36d4b81668f">IKEEXT_COOKIE_PAIR0</a></b>

The SA cookies.


### -field ikeCredentials

Type: <b><a href="https://msdn.microsoft.com/4099b6e7-0b3b-40ea-821c-3ff28a6f788f">IKEEXT_CREDENTIALS2</a></b>

Credentials information for the SA.


### -field ikePolicyKey

Type: <b>GUID</b>

GUID of the main mode policy provider context corresponding to this SA.


### -field virtualIfTunnelId

Type: <b>UINT64</b>

ID/Handle to virtual interface tunneling state. Applicable only to IKEv2.


### -field correlationKey

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a></b>

Key derived from authentications to allow external applications to cryptographically bind
   their exchanges with this SA.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552435">FWP_IP_VERSION</a>



<a href="https://msdn.microsoft.com/c752545b-1880-40ac-871e-e36d4b81668f">IKEEXT_COOKIE_PAIR0</a>



<a href="https://msdn.microsoft.com/4099b6e7-0b3b-40ea-821c-3ff28a6f788f">IKEEXT_CREDENTIALS2</a>



<a href="https://msdn.microsoft.com/a9268b07-343a-4a51-bc70-3e624facf617">IKEEXT_KEY_MODULE_TYPE</a>



<a href="https://msdn.microsoft.com/59568ef7-12bd-407a-a8ee-9bf261f49883">IKEEXT_PROPOSAL0</a>



<a href="https://msdn.microsoft.com/99cb3774-7afd-44fd-9c3e-e2d913aaeecb">IKEEXT_TRAFFIC0</a>



<a href="https://msdn.microsoft.com/69cddec0-7311-4833-8b24-293ad714054e">IPSEC_V4_UDP_ENCAPSULATION0</a>
 

 

