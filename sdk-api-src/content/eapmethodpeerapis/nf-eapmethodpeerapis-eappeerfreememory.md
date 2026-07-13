---
UID: NF:eapmethodpeerapis.EapPeerFreeMemory
title: EapPeerFreeMemory function (eapmethodpeerapis.h)
description: Releases all memory associated with an opaque user interface context data buffer. (EapPeerFreeMemory)
helpviewer_keywords: ["EapPeerFreeMemory","EapPeerFreeMemory function [EAPHost]","eaphost.eappeerfreememory","eapmethodpeerapis/EapPeerFreeMemory"]
old-location: eaphost\eappeerfreememory.htm
tech.root: eaphost
ms.assetid: 544d999c-d857-4ca5-b5f8-b15780fc7019
ms.date: 12/05/2018
ms.keywords: EapPeerFreeMemory, EapPeerFreeMemory function [EAPHost], eaphost.eappeerfreememory, eapmethodpeerapis/EapPeerFreeMemory
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapPeerFreeMemory
 - eapmethodpeerapis/EapPeerFreeMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eapmethodpeerapis.h
api_name:
 - EapPeerFreeMemory
---

# EapPeerFreeMemory function


## -description

Releases all memory associated with an opaque user interface context data buffer.

## -parameters

### -param pUIContextData [in]

A pointer to the user interface context data to free.

## -remarks

This method is called to release the user interface context data provided to the UI-specific EAP peer method APIs.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Peer Method Configuration Functions](/windows/win32/eaphost/eaphost-peer-method-configuration-functions)



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerfreeerrormemory">EapPeerFreeErrorMemory</a>
