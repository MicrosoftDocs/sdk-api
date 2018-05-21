---
UID: NF:eappapis.EapHostPeerGetUIContext
title: EapHostPeerGetUIContext function
author: windows-driver-content
description: Obtains the user interface context for the supplicant from EAPHost if the UI is to be raised.
old-location: eaphost\eaphostpeergetuicontext.htm
old-project: EAPHost
ms.assetid: 47ade6f1-067b-48ab-b4ac-a3d3cf63d809
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: EapHostPeerGetUIContext, EapHostPeerGetUIContext function [EAPHost], eaphost.eaphostpeergetuicontext, eappapis/EapHostPeerGetUIContext
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: EapPacket
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	eappprxy.dll
api_name:
-	EapHostPeerGetUIContext
product: Windows
targetos: Windows
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapHostPeerGetUIContext function


## -description


Obtains the user interface context for the supplicant from EAPHost if the UI is to be raised.

<b>EAPHostPeerGetUIContext</b> is always followed by the following functions.<ul>
<li>
<a href="https://msdn.microsoft.com/a4a46b77-f8ab-4062-b966-1590ea9e46d2">EapHostPeerInvokeInteractiveUI</a>, and</li>
<li>
<a href="https://msdn.microsoft.com/f532dd65-d807-4880-9339-ba233e0faa38">EapHostPeerSetUIContext</a>
</li>
</ul>



## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>.


### -param pdwSizeOfUIContextData [out]

A pointer to a value that specifies the size, in bytes, of the UI context data  buffer returned in <i>ppUIContextData</i>.


### -param ppUIContextData [out]

A pointer to a pointer to a  buffer that contains the supplicant UI context data from EAPHost. The address pointed to by this parameter is passed to <a href="https://msdn.microsoft.com/a4a46b77-f8ab-4062-b966-1590ea9e46d2">EapHostPeerInvokeInteractiveUI</a> as IN parameter <i>pUIContextData</i>.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeEapError</a>.


## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-time Functions</a>



<a href="https://msdn.microsoft.com/a4a46b77-f8ab-4062-b966-1590ea9e46d2">EapHostPeerInvokeInteractiveUI</a>



<a href="https://msdn.microsoft.com/f532dd65-d807-4880-9339-ba233e0faa38">EapHostPeerSetUIContext</a>
 

 

