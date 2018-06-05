---
UID: NS:raseapif._PPP_EAP_INFO
title: "_PPP_EAP_INFO"
author: windows-sdk-content
description: The PPP_EAP_INFO structure provides information to the Connection Manager about the authentication protocol, including pointers to functions located in the EAP DLL.
old-location: eap\ppp_eap_info.htm
old-project: EAP
ms.assetid: 722e8185-3408-418b-ae80-e2ed261edcd1
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PPPP_EAP_INFO, PPPP_EAP_INFO, PPPP_EAP_INFO structure pointer [EAP], PPP_EAP_INFO, PPP_EAP_INFO structure [EAP], _PPP_EAP_INFO, _eap_ppp_eap_info, eap.ppp_eap_info, raseapif/PPPP_EAP_INFO, raseapif/PPP_EAP_INFO"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
req.product: Rights Management Services client 1.0 or later
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



#### fInitialize

Specifies whether the authentication protocol should initialize or de-initialize. This parameter is <b>TRUE</b> if the protocol initializes and <b>FALSE</b> if the protocol does not initialize.


### -field RasEapBegin

Pointer to the 
<a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a> function for the requested authentication protocol. The authentication protocol sets the value of this member. This member may be <b>NULL</b>, in which case, the authentication protocol does not require any initialization. If this member is <b>NULL</b>, RAS ignores the <b>RasEapEnd</b> member.



#### ppWorkBuffer

Pointer to a pointer that, on successful return, points to a work buffer. This buffer is opaque to RAS; the contents of the buffer are used only by the authentication protocol. The RAS connection manager passes a pointer to this buffer to the authentication protocol in subsequent calls to 
<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a>.



#### pPppEapInput

Pointer to a 
<a href="https://msdn.microsoft.com/80a8f118-323d-4040-91f7-202eeee6d227">PPP_EAP_INPUT</a> structure that specifies initialization information for the authentication session.


### -field RasEapEnd

Pointer to the 
<a href="https://msdn.microsoft.com/52204bc6-03ed-4e8c-819f-b54174ccdbd4">RasEapEnd</a> function for the authentication protocol. The authentication protocol sets the value of this member.



#### pWorkBuffer

Pointer to the work buffer to free.


### -field RasEapMakeMessage

Pointer to the 
<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a> function for the requested authentication protocol. The authentication protocol sets the value of this member.



#### pWorkBuf

Pointer to the work buffer. The authentication protocol provides RAS with a pointer to this buffer via the 
<a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a> function.



#### pReceivePacket

Pointer to a 
<a href="https://msdn.microsoft.com/a1ca16d1-bf91-4986-a4f8-6e6ad382730f">PPP_EAP_PACKET</a> structure that contains a received packet. A <i>pReceivePacket</i> value of <b>NULL</b> indicates either that RAS is initiating the dialog with the authentication protocol, or that a time out has occurred and the authentication protocol should resend the last packet. The authentication protocol must determine, based on context, which of these two cases is true.



#### pSendPacket

Pointer to a 
<a href="https://msdn.microsoft.com/a1ca16d1-bf91-4986-a4f8-6e6ad382730f">PPP_EAP_PACKET</a> structure. The authentication protocol can use this structure to specify a packet to send.



#### cbSendPacket

Specifies the size, in bytes, of the buffer pointed to by <i>pSendPacket</i>.



#### pEapOutput

Pointer to a 
<a href="https://msdn.microsoft.com/d1634973-f6af-4be3-914a-513098c5fccf">PPP_EAP_OUTPUT</a> structure.



#### pEapInput

Pointer to a 
<a href="https://msdn.microsoft.com/80a8f118-323d-4040-91f7-202eeee6d227">PPP_EAP_INPUT</a> structure. This parameter may be <b>NULL</b>.


## -remarks



A given EAP DLL may implement more than one authentication protocol. Use the <b>dwEapTypeId</b> member to specify for which protocol to retrieve information.




## -see-also




<a href="https://msdn.microsoft.com/f2f1cf75-18d4-4764-a747-24662f166eb7">EAP Structures</a>



<a href="https://msdn.microsoft.com/d3cb25ce-6fb9-4fca-8662-3efef14238a5">Extensible Authentication Protocol Reference</a>



<a href="https://msdn.microsoft.com/f5f9be64-25c5-42c8-8a08-1457e04e3c45">RasEapBegin</a>



<a href="https://msdn.microsoft.com/52204bc6-03ed-4e8c-819f-b54174ccdbd4">RasEapEnd</a>



<a href="https://msdn.microsoft.com/e75964b9-f5d6-494e-8620-07f0e97bcd09">RasEapGetInfo</a>



<a href="https://msdn.microsoft.com/8e38c155-2fa0-42c8-a843-c90e4f3f8854">RasEapMakeMessage</a>
 

 

