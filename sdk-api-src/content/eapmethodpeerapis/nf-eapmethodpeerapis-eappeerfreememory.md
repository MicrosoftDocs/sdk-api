---
UID: NF:eapmethodpeerapis.EapPeerFreeMemory
title: EapPeerFreeMemory function
author: windows-sdk-content
description: Releases all memory associated with an opaque user interface context data buffer.
old-location: eaphost\eappeerfreememory.htm
old-project: eaphost
ms.assetid: 544d999c-d857-4ca5-b5f8-b15780fc7019
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EapPeerFreeMemory, EapPeerFreeMemory function [EAPHost], eaphost.eappeerfreememory, eapmethodpeerapis/EapPeerFreeMemory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: eapmethodpeerapis.h
req.include-header: 
req.redist: 
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
req.typenames: EAP_AUTHENTICATOR_METHOD_ROUTINES, *PEAP_AUTHENTICATOR_METHOD_ROUTINES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerFreeMemory
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapPeerFreeMemory function


## -description


Releases all memory associated with an opaque user interface context data buffer.


## -parameters




### -param pUIContextData [in]

A pointer to the user interface context data to free.


## -returns



This function does not return a value.




## -remarks



This method is called to release the user interface context data provided to the UI-specific EAP peer method APIs.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/ba5c90b2-5185-4810-84a2-d08e62e8105c">EAPHost Peer Method Configuration Functions</a>



<a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>
 

 

