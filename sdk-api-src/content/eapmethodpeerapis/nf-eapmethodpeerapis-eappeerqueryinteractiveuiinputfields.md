---
UID: NF:eapmethodpeerapis.EapPeerQueryInteractiveUIInputFields
title: EapPeerQueryInteractiveUIInputFields function (eapmethodpeerapis.h)
author: windows-sdk-content
description: Defines the implementation of an EAP method API that provides the input fields for interactive UI components to be raised on the supplicant.
old-location: eaphost\eappeerqueryinteractiveuiinputfields.htm
tech.root: eaphost
ms.assetid: 7019e13f-d5ad-40ba-8e70-8ded4b136d6c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EapPeerQueryInteractiveUIInputFields, EapPeerQueryInteractiveUIInputFields function [EAPHost], eaphost.eappeerqueryinteractiveuiinputfields, eapmethodpeerapis/EapPeerQueryInteractiveUIInputFields
ms.topic: function
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
 - EapPeerQueryInteractiveUIInputFields
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EapPeerQueryInteractiveUIInputFields function


## -description


The <b>EapPeerQueryInteractiveUIInputFields</b> function defines the implementation of an EAP method API that provides the input fields for interactive UI components to be raised on the supplicant.


## -parameters




### -param dwVersion [in]

The version number of the API. Must be set to zero.


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param dwSizeofUIContextData [in]

The size of the context data in <i>pUIContextData</i>, in bytes.


### -param pUIContextData [in]

A pointer to a BLOB that contains UI context data, represented as inner pointers to field data. The supplicant obtained these inner pointers from EAPHost run-time APIs.


### -param pEapInteractiveUIData [out]

Pointer that receives an <a href="https://msdn.microsoft.com/68141611-4a1c-409e-8ed2-3d21a76640c3">EAP_INTERACTIVE_UI_DATA</a> structure that  contains configuration information for interactive UI components raised on an EAP supplicant.


### -param ppEapError [out]

 A pointer to the address of an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised during  the execution of this function call. After consuming the error data, this memory must be freed by passing a pointer to the error data to <a href="https://msdn.microsoft.com/85b4197c-5caf-4e2b-94fd-e651712dd39d">EapPeerFreeErrorMemory</a>.


### -param ppvReserved [in, out]

Reserved for future usage. Must be set to <b>NULL</b>


## -remarks




<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">EapPeerQueryInteractiveUIInputFields</a> can be employed to support Single-Sign-On (SSO). The <b>EAP_FLAG_PRE_LOGON</b> flag in <a href="https://msdn.microsoft.com/770a548c-c227-4708-bc40-08bf2681c90f">EapPeerBeginSession</a> indicates to EAPHost that SSO should be provided. If the <b>EapPeerResponseInvokeUI</b> action code is received after calling <b>EapPeerBeginSession</b>, EAPHost then calls <b>EapPeerQueryInteractiveUIInputFields</b>, and later calls <a href="https://msdn.microsoft.com/bfb8906e-7adb-4c69-bd13-7c5239d392af">EapPeerQueryUIBlobFromInteractiveUIInputFields</a>.

The supplicant should call  always call the <b>EapPeerQueryInteractiveUIInputFields</b> function first after receiving the <b>EapPeerResponseInvokeUI</b> action code from EAPHost. If the <b>EapPeerResponseInvokeUI</b> action code  isn't returned, or if   <a href="https://msdn.microsoft.com/081b7a72-abe3-4cbb-9b6c-07bb6717fbfe">EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED</a> is returned, the supplicant should resort to the traditional model of invoking method interactive UI by calling <a href="https://msdn.microsoft.com/16301c49-4415-4ebe-abdd-a03183db5f20">EapPeerInvokeInteractiveUI</a>. If there is an error, <b>EapPeerQueryInteractiveUIInputFields</b> will return a return code other than <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/e8a2e934-1ded-4159-8cd8-7aeb75ce743a">EAP_CONFIG_INPUT_FIELD_ARRAY</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

