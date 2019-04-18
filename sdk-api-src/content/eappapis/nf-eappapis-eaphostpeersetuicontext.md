---
UID: NF:eappapis.EapHostPeerSetUIContext
title: EapHostPeerSetUIContext function (eappapis.h)
author: windows-sdk-content
description: Provides a new or updated user interface context to the EAP peer method loaded on EAPHost after the UI has been raised.
old-location: eaphost\eaphostpeersetuicontext.htm
tech.root: eaphost
ms.assetid: f532dd65-d807-4880-9339-ba233e0faa38
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapHostPeerSetUIContext, EapHostPeerSetUIContext function [EAPHost], eaphost.eaphostpeersetuicontext, eappapis/EapHostPeerSetUIContext
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
req.lib: Eappprxy.lib
req.dll: Eappprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappprxy.dll
api_name:
 - EapHostPeerSetUIContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapHostPeerSetUIContext function


## -description


Provides a new or updated user interface context to the EAP peer method loaded on EAPHost after the UI has been raised. For more information about raising the UI, see <a href="https://msdn.microsoft.com/47ade6f1-067b-48ab-b4ac-a3d3cf63d809">EapHostPeerGetUIContext</a>.

<b>EapHostPeerSetUIContext</b> sets the UI context data that was received from a call to <a href="https://msdn.microsoft.com/a4a46b77-f8ab-4062-b966-1590ea9e46d2">EapHostPeerInvokeInteractiveUI</a>.


## -parameters




### -param sessionHandle [in]

A pointer to an <b>EAP_SESSIONID</b> structure that contains the unique handle for this EAP authentication session on the EAPHost server. This handle is returned in the <i>pSessionId</i> parameter in a previous call to <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a>.


### -param dwSizeOfUIContextData [in]

The size, in bytes, of the user interface context data buffer provided in <i>pUIContextData</i>.


### -param pUIContextData [in]

A pointer to a byte buffer that contains the new supplicant UI context data to be set on EAPHost. The data is returned from the <a href="https://msdn.microsoft.com/a4a46b77-f8ab-4062-b966-1590ea9e46d2">EapHostPeerInvokeInteractiveUI</a> OUT parameter.


### -param pEapOutput [out]

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa363575(v=VS.85).aspx">EapHostPeerResponseAction</a> enumeration value that specifies the action code for the next step the supplicant must take as a response.


### -param ppEapError [out]

A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure. The address should be set to <b>NULL</b> before calling this function. If error data is available, a pointer to the address of an <b>EAP_ERROR</b> structure that contains any errors raised during the execution of this function call is received. After using the error data, free this memory by calling <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeEapError</a>.


## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-time Functions</a>



<a href="https://msdn.microsoft.com/47ade6f1-067b-48ab-b4ac-a3d3cf63d809">EapHostPeerGetUIContext</a>



<a href="https://msdn.microsoft.com/a4a46b77-f8ab-4062-b966-1590ea9e46d2">EapHostPeerInvokeInteractiveUI</a>
 

 

