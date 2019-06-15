---
UID: NF:eaphostpeerconfigapis.EapHostPeerFreeMemory
title: EapHostPeerFreeMemory function (eaphostpeerconfigapis.h)
author: windows-sdk-content
description: Frees memory returned by the configuration APIs.
old-location: eaphost\eaphostpeerfreememory.htm
tech.root: eaphost
ms.assetid: 162c796c-b9dc-465a-a1bc-f11d740f3fa0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapHostPeerFreeMemory, EapHostPeerFreeMemory function [EAPHost], eaphost.eaphostpeerfreememory, eaphostpeerconfigapis/EapHostPeerFreeMemory
ms.topic: function
f1_keywords: ["eaphostpeerconfigapis/EapHostPeerFreeMemory"]
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
ms.custom: 19H1
---

# EapHostPeerFreeMemory function


## -description


 Frees memory returned by the configuration APIs.  Do not use this function to free memory allocated to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_error">EAP_ERROR</a> structure. Use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a> to free error memory.


## -parameters




### -param pData

A pointer to the memory to free.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-host-supplicant-configuration-functions">EAPHost Supplicant Configuration Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eaphost-supplicant-frequently-asked-questions">EAPHost Supplicant Frequently Asked Questions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a>
 

 

