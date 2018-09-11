---
UID: NF:eaphostpeerconfigapis.EapHostPeerGetMethods
title: EapHostPeerGetMethods function
author: windows-sdk-content
description: Enumerates all EAP methods installed and available for use, including legacy EAP Methods.
old-location: eaphost\eaphostpeergetmethods.htm
tech.root: eaphost
ms.assetid: 5b2b351b-d6d8-406c-aa9f-ac720def3681
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EapHostPeerGetMethods, EapHostPeerGetMethods function [EAPHost], eaphost.eaphostpeergetmethods, eaphostpeerconfigapis/EapHostPeerGetMethods
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
 - EapHostPeerGetMethods
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EapHostPeerGetMethods function


## -description


Enumerates all EAP methods installed and available for use, including legacy EAP Methods. 


## -parameters




### -param pEapMethodInfoArray [out]

 A pointer  to an <a href="https://msdn.microsoft.com/a3e2d5c0-eacd-46de-b092-6fd749870881">EAP_METHOD_INFO_ARRAY</a> structure for installed EAP methods. The caller should free the inner pointers
                using the function <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>, starting at the innermost pointer.


### -param ppEapError [out]

 
A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeErrorMemory</a>.


## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>
 

 

