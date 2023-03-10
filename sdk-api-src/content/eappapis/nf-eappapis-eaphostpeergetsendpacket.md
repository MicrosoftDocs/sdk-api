---
UID: NF:eappapis.EapHostPeerGetSendPacket
title: EapHostPeerGetSendPacket function (eappapis.h)
description: Is called by the supplicant when the supplicant needs to obtains a packet from EAPHost to send to the authenticator.
helpviewer_keywords: ["EapHostPeerGetSendPacket","EapHostPeerGetSendPacket function [EAPHost]","eaphost.eaphostpeergetsendpacket","eappapis/EapHostPeerGetSendPacket"]
old-location: eaphost\eaphostpeergetsendpacket.htm
tech.root: eaphost
ms.assetid: 22e17496-e381-415e-8da0-88aad37d0d21
ms.date: 12/05/2018
ms.keywords: EapHostPeerGetSendPacket, EapHostPeerGetSendPacket function [EAPHost], eaphost.eaphostpeergetsendpacket, eappapis/EapHostPeerGetSendPacket
req.header: eappapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerGetSendPacket
 - eappapis/EapHostPeerGetSendPacket
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerGetSendPacket
---

# EapHostPeerGetSendPacket function


## -description

Is called by the supplicant when the supplicant needs to obtains a packet 
   from EAPHost to send to the authenticator. <b>EapHostPeerGetSendPacket</b> is called when the supplicant receives the <a href="/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerresponseaction">EapHostPeerResponseAction</a>  enumerator from the server.

## -parameters

### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession">EapHostPeerBeginSession</a>.

### -param pcbSendPacket [out]

A pointer to a DWORD that specifies the maximum size, in bytes,  of the buffer pointed to by   <i>ppSendPacket</i>. <b>EapHostPeerGetSendPacket</b> on return is the size of the actual data pointed to by <i>ppSendPacket</i>.

### -param ppSendPacket [out]

A pointer to a pointer to a  buffer that contains the packet data returned by the EAP module. The buffer is allocated by EAPHost.

### -param ppEapError [out]

A pointer to the address of an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerfreeeaperror">EapHostPeerFreeEapError</a>.

## -see-also

[EAPHost Supplicant Run-time Functions](/windows/win32/eaphost/eap-host-supplicant-run-time-functions)