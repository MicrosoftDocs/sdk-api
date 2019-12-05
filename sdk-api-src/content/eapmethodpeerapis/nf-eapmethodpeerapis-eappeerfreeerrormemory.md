---
UID: NF:eapmethodpeerapis.EapPeerFreeErrorMemory
title: EapPeerFreeErrorMemory function (eapmethodpeerapis.h)
description: Releases error-specific memory allocated by the EAP peer method.
old-location: eaphost\eappeerfreeerrormemory.htm
tech.root: eaphost
ms.assetid: 85b4197c-5caf-4e2b-94fd-e651712dd39d
ms.date: 12/05/2018
ms.keywords: EapPeerFreeErrorMemory, EapPeerFreeErrorMemory function [EAPHost], eaphost.eappeerfreeerrormemory, eapmethodpeerapis/EapPeerFreeErrorMemory
ms.topic: function
f1_keywords:
- eapmethodpeerapis/EapPeerFreeErrorMemory
dev_langs:
- c++
req.header: eapmethodpeerapis.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- eapmethodpeerapis.h
api_name:
- EapPeerFreeErrorMemory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapPeerFreeErrorMemory function


## -description


Releases error-specific memory allocated by the EAP peer method.


## -parameters




### -param pEapError [in]

A pointer to the address of an <a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains the error data to free.


## -returns



This function does not return a value.




## -remarks



This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




[EAPHost Peer Method Configuration Functions](https://docs.microsoft.com/windows/win32/eaphost/eaphost-peer-method-configuration-functions)a>



<a href="https://docs.microsoft.com/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreememory">EapPeerFreeMemory</a>
 

 

