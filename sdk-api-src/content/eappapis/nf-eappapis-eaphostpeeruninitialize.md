---
UID: NF:eappapis.EapHostPeerUninitialize
title: EapHostPeerUninitialize function
author: windows-sdk-content
description: Uninitializes all EAPHost authentication sessions.
old-location: eaphost\eaphostpeeruninitialize.htm
tech.root: EAPHost
ms.assetid: 5d3a101a-4de3-4da2-8c03-e672e206ffb0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EapHostPeerUninitialize, EapHostPeerUninitialize function [EAPHost], eaphost.eaphostpeeruninitialize, eappapis/EapHostPeerUninitialize
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
 - EapHostPeerUninitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- EapHostPeerUninitialize
: 
---

# EapHostPeerUninitialize function


## -description


Uninitializes all  EAPHost authentication sessions. 

The <b>EapHostPeerUninitialize</b> function must be called after you are finished calling EAPHost supplicant run-time functions. In addition, if any re-authentication is expected for any reason it is best to call <b>EapHostPeerUninitialize</b>.


## -parameters






## -returns



This function does not return a value.




## -remarks




<a href="https://msdn.microsoft.com/4af7103e-85c8-472e-96fe-407f07a1f447">EapHostPeerInitialize</a> and <b>EapHostPeerUninitialize</b> are always thread
safe.

<b>EapHostPeerUninitialize</b> calls <b>CoUninitialize</b>.




## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-time Functions</a>



<a href="https://msdn.microsoft.com/4af7103e-85c8-472e-96fe-407f07a1f447">EapHostPeerInitialize</a>
 

 

