---
UID: NF:eaphostpeerconfigapis.EapHostPeerQueryInteractiveUIInputFields
title: EapHostPeerQueryInteractiveUIInputFields function
author: windows-sdk-content
description: Obtains the input fields for interactive UI components to be raised on the supplicant.
old-location: eaphost\eaphostpeerqueryinteractiveuiinputfields.htm
old-project: eaphost
ms.assetid: facf4ccf-c2e3-435e-8333-8d2c5bbe0186
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EAPHOST_PEER_API_VERSION, EapHostPeerQueryInteractiveUIInputFields, EapHostPeerQueryInteractiveUIInputFields function [EAPHost], eaphost.eaphostpeerqueryinteractiveuiinputfields, eaphostpeerconfigapis/EapHostPeerQueryInteractiveUIInputFields
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: eaphostpeerconfigapis.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EAP_AUTHENTICATOR_SEND_TIMEOUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapHostPeerQueryInteractiveUIInputFields
product: Windows
targetos: Windows
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapHostPeerQueryInteractiveUIInputFields function


## -description


The <b>EapHostPeerQueryInteractiveUIInputFields</b> function obtains the input fields for interactive UI components to be raised on the supplicant.


## -parameters




### -param dwVersion [in]

The version number of the API. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EAPHOST_PEER_API_VERSION"></a><a id="eaphost_peer_api_version"></a><dl>
<dt><b>EAPHOST_PEER_API_VERSION</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The version of the EAPHost peer API.

</td>
</tr>
</table>
 


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param dwSizeofUIContextData [in]

The size of the context data in <i>pUIContextData</i>, in bytes.


### -param pUIContextData [in]

Pointer to a BLOB that contains UI context data, represented as inner pointers to field data. These inner pointers must be freed by passing them to <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>, starting with the innermost pointer.


### -param pEapInteractiveUIData [out]

Pointer that receives an <a href="https://msdn.microsoft.com/68141611-4a1c-409e-8ed2-3d21a76640c3">EAP_INTERACTIVE_UI_DATA</a> structure that contains configuration information for interactive UI components raised on an EAP supplicant. The caller should free the inner pointers
                using the function <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>, starting at the innermost pointer.


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a>.


### -param ppvReserved [in, out]

Reserved for future use. This parameter must be set to 0.


## -remarks



<b>EapHostPeerQueryInteractiveUIInputFields</b> can be employed to support Single-Sign-On (SSO). The supplicant  uses the <b>EAP_FLAG_PRE_LOGON</b> flag in <a href="https://msdn.microsoft.com/9dc339bc-ef01-4432-83cb-b4b14a36f18e">EapHostPeerBeginSession</a> to indicate to EAPHost that SSO should be provided. If the <a href="https://msdn.microsoft.com/59bf6e02-90b5-4f9a-9865-b71852c61db9">EapHostPeerResponseInvokeUI</a> action code is received after calling <b>EapHostPeerBeginSession</b>, EAPHost then calls <b>EapHostPeerQueryInteractiveUIInputFields</b>, and later calls <a href="https://msdn.microsoft.com/2c4b1a0b-8c3f-47c5-8829-2f9c9bfda946">EapHostPeerQueryUIBlobFromInteractiveUIInputFields</a>. 

The supplicant should call the <b>EapHostPeerQueryInteractiveUIInputFields</b> function first after receiving the <a href="https://msdn.microsoft.com/59bf6e02-90b5-4f9a-9865-b71852c61db9">EapHostPeerResponseInvokeUI</a> action code from EAPHost. If the EapHostPeerResponseInvokeUI action code  isn't returned, or if  <a href="https://msdn.microsoft.com/081b7a72-abe3-4cbb-9b6c-07bb6717fbfe">EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED</a> is returned, the supplicant should resort to the traditional model of invoking method interactive UI by calling <a href="https://msdn.microsoft.com/a4a46b77-f8ab-4062-b966-1590ea9e46d2">EapHostPeerInvokeInteractiveUI</a>. If there is an error, <b>EapHostPeerQueryInteractiveUIInputFields</b> will return a return code other than <b>NULL</b>. 




## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c">SSO and PLAP</a>
 

 

