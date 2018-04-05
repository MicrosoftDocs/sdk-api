---
UID: NF:eaphostpeerconfigapis.EapHostPeerFreeErrorMemory
title: EapHostPeerFreeErrorMemory function
author: windows-driver-content
description: Frees memory allocated to an EAP_ERROR structure.
old-location: eaphost\eaphostpeerfreeerrormemory.htm
old-project: EAPHost
ms.assetid: c80ac625-8202-49a7-813a-62a9e0d15058
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: EapHostPeerFreeErrorMemory, EapHostPeerFreeErrorMemory function [EAPHost], eaphost.eaphostpeerfreeerrormemory, eaphostpeerconfigapis/EapHostPeerFreeErrorMemory
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
req.typenames: EAP_AUTHENTICATOR_SEND_TIMEOUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	eappcfg.dll
api_name:
-	EapHostPeerFreeErrorMemory
product: Windows
targetos: Windows
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapHostPeerFreeErrorMemory function


## -description


Frees memory allocated to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure.  An  <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP ERROR</a> structure is created whenever an <a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost supplicant configuration function</a> fails. 

The  <b>EapHostPeerFreeErrorMemory</b> function is used only for freeing <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structures returned by EAPHost configuration APIs, while the <a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostPeerFreeEapError</a> function is used for freeing <b>EAP_ERROR</b> structures returned by EAPHost run-time APIs.

If any  of the following configuration APIs functions are called, and an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> is returned, <b>EapHostPeerFreeErrorMemory</b> must be called to free the memory:<ul>
<li>
<a href="https://msdn.microsoft.com/158750ec-cc26-4740-add6-2135b9aa294c">EapHostPeerConfigBlob2Xml</a>
</li>
<li>
<a href="https://msdn.microsoft.com/728fab9e-6aa4-49c0-ab1f-89686543524c">EapHostPeerConfigXml2Blob</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ef8475f0-047d-4858-b3c1-3ddf41c1847f">EapHostPeerCredentialsXml2Blob</a>
</li>
<li>
<a href="https://msdn.microsoft.com/afb20482-a439-437d-9c8f-c4e87e440113">EapHostPeerInvokeConfigUI</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f71aad69-89f3-463b-afd7-9873d582d03b">EapHostPeerQueryCredentialsInputFields</a>
</li>
<li>
<a href="https://msdn.microsoft.com/bd4fafce-7ece-4cdc-9307-4d41538a4f49">EapHostPeerQueryUserBlobFromCredentialsInputFields</a>
</li>
</ul>

<div class="alert"><b>Note</b>  EAPHost run-time APIs are defined in eappapis.h. EAPHost configuration APIs are defined in  EapHostPeerConfigApis.h. </div><div> </div>

## -parameters




### -param pEapError

A pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that  contains the error data to free.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>



<a href="https://msdn.microsoft.com/bf8db711-386e-47c2-be47-4cfd6c4d8d9e">EAPHost Supplicant Frequently Asked Questions</a>



<a href="https://msdn.microsoft.com/36f9b5dd-821d-4cc5-a1dd-587098635d17">EapHostFreeEapError</a>
 

 

