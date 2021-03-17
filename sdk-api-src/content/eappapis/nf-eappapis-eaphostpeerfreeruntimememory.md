---
UID: NF:eappapis.EapHostPeerFreeRuntimeMemory
title: EapHostPeerFreeRuntimeMemory function (eappapis.h)
description: Releases the memory space used during run-time.
helpviewer_keywords: ["EapHostPeerFreeRuntimeMemory","EapHostPeerFreeRuntimeMemory function [EAPHost]","eaphost.eaphostpeerfreeruntimememory","eappapis/ EapHostPeerFreeRuntimeMemory"]
old-location: eaphost\eaphostpeerfreeruntimememory.htm
tech.root: eaphost
ms.assetid: d27233a0-b41f-43f6-a934-1ab8df8b0581
ms.date: 12/05/2018
ms.keywords: EapHostPeerFreeRuntimeMemory, EapHostPeerFreeRuntimeMemory function [EAPHost], eaphost.eaphostpeerfreeruntimememory, eappapis/ EapHostPeerFreeRuntimeMemory
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
req.dll: Eapphost.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerFreeRuntimeMemory
 - eappapis/EapHostPeerFreeRuntimeMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eapphost.dll
api_name:
 - EapHostPeerFreeRuntimeMemory
---

# EapHostPeerFreeRuntimeMemory function


## -description

Releases the memory space used during run-time.

## -parameters

### -param pData [in]

A pointer to a buffer returned by any EapHost peer run-time API.

## -remarks

This method is called to release a specified memory buffer returned by any  EAPHost peer run-time APIs.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.

## -see-also

[EAPHost Supplicant Run-Time Functions](/windows/win32/eaphost/eap-host-supplicant-run-time-functions)



<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeidentityui">EapHostPeerInvokeIdentityUI</a>