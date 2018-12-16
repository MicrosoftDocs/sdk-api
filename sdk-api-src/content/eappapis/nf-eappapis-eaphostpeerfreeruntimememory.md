---
UID: NF:eappapis.EapHostPeerFreeRuntimeMemory
title: EapHostPeerFreeRuntimeMemory function
author: windows-sdk-content
description: Releases the memory space used during run-time.
old-location: eaphost\eaphostpeerfreeruntimememory.htm
tech.root: eaphost
ms.assetid: d27233a0-b41f-43f6-a934-1ab8df8b0581
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EapHostPeerFreeRuntimeMemory, EapHostPeerFreeRuntimeMemory function [EAPHost], eaphost.eaphostpeerfreeruntimememory, eappapis/ EapHostPeerFreeRuntimeMemory
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
req.dll: Eapphost.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eapphost.dll
api_name:
 - EapHostPeerFreeRuntimeMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapHostPeerFreeRuntimeMemory function


## -description


Releases the memory space used during run-time.


## -parameters




### -param pData [in]

A pointer to a buffer returned by any EapHost peer run-time API.


## -returns



This function does not return a value. 




## -remarks



This method is called to release a specified memory buffer returned by any  EAPHost peer run-time APIs.

This call is performed by a peer-based EAPHost using a function pointer to this API. This API must be implemented on the EAP method loaded by EAPHost, and must strictly conform to the syntax and parameter types specified in the documentation.




## -see-also




<a href="https://msdn.microsoft.com/b1c473ba-9a12-4929-b4d0-27262117e9c0">EAPHost Supplicant Run-Time Functions</a>



<a href="https://msdn.microsoft.com/48c48162-44d8-45d2-9147-5bf006d493b5">EapHostPeerInvokeIdentityUI</a>
 

 

