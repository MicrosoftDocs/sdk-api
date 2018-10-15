---
UID: NS:ipsectypes.IPSEC_SA_DETAILS0_
title: IPSEC_SA_DETAILS0_
author: windows-sdk-content
description: Is used to store information returned when enumerating IPsec security associations (SAs).
old-location: fwp\ipsec_sa_details0_struct.htm
tech.root: fwp
ms.assetid: 261cea6e-4a56-404f-9e5d-70ce95122f9f
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IPSEC_SA_DETAILS0, IPSEC_SA_DETAILS0 structure [Filtering], IPSEC_SA_DETAILS0_, fwp.ipsec_sa_details0_struct, ipsectypes/IPSEC_SA_DETAILS0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
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
 - Ipsectypes.h
api_name:
 - IPSEC_SA_DETAILS0
product: Windows
targetos: Windows
req.typenames: IPSEC_SA_DETAILS0
req.redist: 
---

# IPSEC_SA_DETAILS0_ structure


## -description


The <b>IPSEC_SA_DETAILS0</b> structure is used to store information returned when enumerating IPsec security associations (SAs).
<div class="alert"><b>Note</b>  <b>IPSEC_SA_DETAILS0</b> is the specific implementation of IPSEC_SA_DETAILS used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/257e7ac0-9cb4-45aa-b7e5-107bb3483ab9">IPSEC_SA_DETAILS1</a> is available.</div><div> </div>

## -struct-fields




### -field ipVersion

Internet Protocol (IP) version as specified by <a href="https://msdn.microsoft.com/1712b83c-f32d-4981-9950-ab870a376182">FWP_IP_VERSION</a>. 


### -field saDirection

Indicates direction of the IPsec SA as specified by <a href="https://msdn.microsoft.com/ae0eeb36-1a41-426a-9878-77558464a91b">FWP_DIRECTION</a>.


### -field traffic

The traffic being secured by this IPsec SA as specified by <a href="https://msdn.microsoft.com/5be2da29-73d6-4381-8bde-3a3945ea7b5a">IPSEC_TRAFFIC0</a>. 


### -field saBundle

Various parameters of the SA as specified by <a href="https://msdn.microsoft.com/65376dd9-e06c-41ff-8689-74be12c47239">IPSEC_SA_BUNDLE0</a>.


### -field udpEncapsulation

An <a href="https://msdn.microsoft.com/69cddec0-7311-4833-8b24-293ad714054e">IPSEC_V4_UDP_ENCAPSULATION0</a> structure that stores the UDP 
   encapsulation ports if UDP-ESP encapsulation is enabled on the SA.

Available if <b>ipVersion</b> is <b>FWP_IP_VERSION_V4</b>.


### -field transportFilter

The transport layer filter corresponding to this IPsec SA as specified by <a href="https://msdn.microsoft.com/e1925824-01c2-426a-a8f0-4d5882812a9e">FWPM_FILTER0</a>.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

