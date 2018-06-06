---
UID: NF:eappapis.EapHostPeerGetSendPacket
title: EapHostPeerGetSendPacket function
author: windows-sdk-content
description: Is called by the supplicant when the supplicant needs to obtains a packet from EAPHost to send to the authenticator.
old-location: eaphost\eaphostpeergetsendpacket.htm
old-project: EAPHost
ms.assetid: 22e17496-e381-415e-8da0-88aad37d0d21
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: EapHostPeerGetSendPacket, EapHostPeerGetSendPacket function [EAPHost], eaphost.eaphostpeergetsendpacket, eappapis/EapHostPeerGetSendPacket
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: EapPacket
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerGetSendPacket
product: Windows
targetos: Windows
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapHostPeerGetSendPacket function


## -description


Is called by the supplicant when the supplicant needs to obtains a packet 
   from EAPHost to send to the authenticator. <b>EapHostPeerGetSendPacket</b> is called when the supplicant receives the <a href="https://msdn.microsoft.com/59bf6e02-90b5-4f9a-9865-b71852c61db9">EapHostPeerResponseAction</a>  enumerator from the server.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>.


### -param pcbSendPacket [out]

A pointer to a DWORD that specifies the maximum size, in bytes,  of the buffer pointed to by   <i>ppSendPacket</i>. <b>EapHostPeerGetSendPacket</b> on return is the size of the actual data pointed to by <i>ppSendPacket</i>.


### -param ppSendPacket [out]

A pointer to a pointer to a  buffer that contains the packet data returned by the EAP module. The buffer is allocated by EAPHost.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeEapError</a>.


## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-time Functions</a>
 

 

