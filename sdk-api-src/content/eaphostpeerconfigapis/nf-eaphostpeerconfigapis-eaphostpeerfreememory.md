---
UID: NF:eaphostpeerconfigapis.EapHostPeerFreeMemory
title: EapHostPeerFreeMemory function
author: windows-sdk-content
description: Frees memory returned by the configuration APIs.
old-location: eaphost\eaphostpeerfreememory.htm
tech.root: eaphost
ms.assetid: 162c796c-b9dc-465a-a1bc-f11d740f3fa0
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: EapHostPeerFreeMemory, EapHostPeerFreeMemory function [EAPHost], eaphost.eaphostpeerfreememory, eaphostpeerconfigapis/EapHostPeerFreeMemory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: eaphostpeerconfigapis.h
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
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapHostPeerFreeMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- EapHostPeerFreeMemory
: 
---

# EapHostPeerFreeMemory function


## -description


 Frees memory returned by the configuration APIs.  Do not use this function to free memory allocated to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure. Use <a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a> to free error memory.


## -parameters




### -param pData

A pointer to the memory to free.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>



<a href="https://msdn.microsoft.com/bf8db711-386e-47c2-be47-4cfd6c4d8d9e">EAPHost Supplicant Frequently Asked Questions</a>



<a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a>
 

 

