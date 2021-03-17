---
UID: NS:raseapif._PPP_EAP_INFO
title: PPP_EAP_INFO (raseapif.h)
description: The PPP_EAP_INFO structure provides information to the Connection Manager about the authentication protocol, including pointers to functions located in the EAP DLL.
helpviewer_keywords: ["*PPPP_EAP_INFO","PPPP_EAP_INFO","PPPP_EAP_INFO structure pointer [EAP]","PPP_EAP_INFO","PPP_EAP_INFO structure [EAP]","_eap_ppp_eap_info","eap.ppp_eap_info","raseapif/PPPP_EAP_INFO","raseapif/PPP_EAP_INFO"]
old-location: eap\ppp_eap_info.htm
tech.root: EAP
ms.assetid: 722e8185-3408-418b-ae80-e2ed261edcd1
ms.date: 12/05/2018
ms.keywords: '*PPPP_EAP_INFO, PPPP_EAP_INFO, PPPP_EAP_INFO structure pointer [EAP], PPP_EAP_INFO, PPP_EAP_INFO structure [EAP], _eap_ppp_eap_info, eap.ppp_eap_info, raseapif/PPPP_EAP_INFO, raseapif/PPP_EAP_INFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PPP_EAP_INFO, *PPPP_EAP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_EAP_INFO
 - raseapif/_PPP_EAP_INFO
 - PPPP_EAP_INFO
 - raseapif/PPPP_EAP_INFO
 - PPP_EAP_INFO
 - raseapif/PPP_EAP_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Raseapif.h
api_name:
 - PPP_EAP_INFO
---

# PPP_EAP_INFO structure


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
<a href="/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)">RasEapInitialize</a> function for the authentication protocol. The authentication protocol sets the value of this member. The authentication protocol may set this member to <b>NULL</b>, in which case the protocol does not require RAS to call this function.



#### fInitialize

Specifies whether the authentication protocol should initialize or de-initialize. This parameter is <b>TRUE</b> if the protocol initializes and <b>FALSE</b> if the protocol does not initialize.

### -field RasEapBegin

Pointer to the 
<a href="/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)">RasEapBegin</a> function for the requested authentication protocol. The authentication protocol sets the value of this member. This member may be <b>NULL</b>, in which case, the authentication protocol does not require any initialization. If this member is <b>NULL</b>, RAS ignores the <b>RasEapEnd</b> member.



#### ppWorkBuffer

Pointer to a pointer that, on successful return, points to a work buffer. This buffer is opaque to RAS; the contents of the buffer are used only by the authentication protocol. The RAS connection manager passes a pointer to this buffer to the authentication protocol in subsequent calls to 
<a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a>.



#### pPppEapInput

Pointer to a 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_input">PPP_EAP_INPUT</a> structure that specifies initialization information for the authentication session.

### -field RasEapEnd

Pointer to the 
<a href="/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)">RasEapEnd</a> function for the authentication protocol. The authentication protocol sets the value of this member.



#### pWorkBuffer

Pointer to the work buffer to free.

### -field RasEapMakeMessage

Pointer to the 
<a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a> function for the requested authentication protocol. The authentication protocol sets the value of this member.



#### pWorkBuf

Pointer to the work buffer. The authentication protocol provides RAS with a pointer to this buffer via the 
<a href="/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)">RasEapBegin</a> function.



#### pReceivePacket

Pointer to a 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_packet">PPP_EAP_PACKET</a> structure that contains a received packet. A <i>pReceivePacket</i> value of <b>NULL</b> indicates either that RAS is initiating the dialog with the authentication protocol, or that a time out has occurred and the authentication protocol should resend the last packet. The authentication protocol must determine, based on context, which of these two cases is true.



#### pSendPacket

Pointer to a 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_packet">PPP_EAP_PACKET</a> structure. The authentication protocol can use this structure to specify a packet to send.



#### cbSendPacket

Specifies the size, in bytes, of the buffer pointed to by <i>pSendPacket</i>.



#### pEapOutput

Pointer to a 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_output">PPP_EAP_OUTPUT</a> structure.



#### pEapInput

Pointer to a 
<a href="/windows/desktop/api/raseapif/ns-raseapif-ppp_eap_input">PPP_EAP_INPUT</a> structure. This parameter may be <b>NULL</b>.

## -remarks

A given EAP DLL may implement more than one authentication protocol. Use the <b>dwEapTypeId</b> member to specify for which protocol to retrieve information.

## -see-also

[EAP Structures](/windows/win32/eap/eap-structures)



[Extensible Authentication Protocol Reference](/windows/win32/eap/extensible-authentication-protocol-reference)



<a href="/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)">RasEapBegin</a>



<a href="/previous-versions/windows/desktop/legacy/aa363521(v=vs.85)">RasEapEnd</a>



<a href="/previous-versions/windows/desktop/api/raseapif/nf-raseapif-raseapgetinfo">RasEapGetInfo</a>



<a href="/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)">RasEapMakeMessage</a>