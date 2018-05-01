---
UID: NS:raseapif._PPP_EAP_INFO
title: "_PPP_EAP_INFO"
author: windows-driver-content
description: The PPP_EAP_INFO structure provides information to the Connection Manager about the authentication protocol, including pointers to functions located in the EAP DLL.
old-location: eap\ppp_eap_info.htm
old-project: EAP
ms.assetid: 722e8185-3408-418b-ae80-e2ed261edcd1
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: "*PPPP_EAP_INFO, PPPP_EAP_INFO, PPPP_EAP_INFO structure pointer [EAP], PPP_EAP_INFO, PPP_EAP_INFO structure [EAP], _PPP_EAP_INFO, _eap_ppp_eap_info, eap.ppp_eap_info, raseapif/PPPP_EAP_INFO, raseapif/PPP_EAP_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: raseapif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PPP_EAP_INFO, *PPPP_EAP_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Raseapif.h
api_name:
-	PPP_EAP_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _PPP_EAP_INFO structure


## -description


The 
<b>PPP_EAP_INFO</b> structure provides information to the Connection Manager about the authentication protocol, including pointers to functions located in the EAP DLL.


## -struct-fields




### -field dwSizeInBytes

Specifies the size of the 
<b>PPP_EAP_INFO</b> structure. RAS passes in this value to the EAP DLL. The DLL uses this value to determine which version of the 
<b>PPP_EAP_INFO</b> structure RAS is using.


### -field dwEapTypeId

Specifies a particular authentication protocol. This identifier must be unique throughout industry-wide implementation of EAP. The implementer of an authentication protocol must obtain this identifier from the Internet Assigned Numbers Authority (IANA).


### -field RasEapInitialize

Pointer to the 
<a href="https://msdn.microsoft.com/f689e89e-b4c4-4167-99ed-0531a6c05267">RasEapInitialize</a> function for the authentication protocol. The authentication protocol sets the value of this member. The authentication protocol may set this member to <b>NULL</b>, in which case the protocol does not require RAS to call this function.


### -field RasEapBegin

Pointer to the 
<a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a> function for the requested authentication protocol. The authentication protocol sets the value of this member. This member may be <b>NULL</b>, in which case, the authentication protocol does not require any initialization. If this member is <b>NULL</b>, RAS ignores the <b>RasEapEnd</b> member.


### -field RasEapEnd

Pointer to the 
<a href="https://msdn.microsoft.com/52204bc6-03ed-4e8c-819f-b54174ccdbd4">RasEapEnd</a> function for the authentication protocol. The authentication protocol sets the value of this member.


### -field RasEapMakeMessage

Pointer to the 
<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a> function for the requested authentication protocol. The authentication protocol sets the value of this member.


## -remarks



A given EAP DLL may implement more than one authentication protocol. Use the <b>dwEapTypeId</b> member to specify for which protocol to retrieve information.




## -see-also




<a href="https://msdn.microsoft.com/f2f1cf75-18d4-4764-a747-24662f166eb7">EAP Structures</a>



<a href="https://msdn.microsoft.com/d3cb25ce-6fb9-4fca-8662-3efef14238a5">Extensible Authentication Protocol Reference</a>



<a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a>



<a href="https://msdn.microsoft.com/52204bc6-03ed-4e8c-819f-b54174ccdbd4">RasEapEnd</a>



<a href="https://msdn.microsoft.com/e75964b9-f5d6-494e-8620-07f0e97bcd09">RasEapGetInfo</a>



<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a>
 

 

