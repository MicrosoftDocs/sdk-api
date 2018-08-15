---
UID: NF:eaphostpeerconfigapis.EapHostPeerQueryUIBlobFromInteractiveUIInputFields
title: EapHostPeerQueryUIBlobFromInteractiveUIInputFields function
author: windows-sdk-content
description: Converts user information into a user BLOB that can be consumed by EAPHost run-time functions.
old-location: eaphost\eaphostpeerqueryuiblobfrominteractiveuiinputfields.htm
old-project: eaphost
ms.assetid: 2c4b1a0b-8c3f-47c5-8829-2f9c9bfda946
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EAPHOST_PEER_API_VERSION, EapHostPeerQueryUIBlobFromInteractiveUIInputFields, EapHostPeerQueryUIBlobFromInteractiveUIInputFields function [EAPHost], eaphost.eaphostpeerqueryuiblobfrominteractiveuiinputfields, eaphostpeerconfigapis/EapHostPeerQueryUIBlobFromInteractiveUIInputFields
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
 - EapHostPeerQueryUIBlobFromInteractiveUIInputFields
product: Windows
targetos: Windows
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EapHostPeerQueryUIBlobFromInteractiveUIInputFields function


## -description


The <b>EapHostPeerQueryUIBlobFromInteractiveUIInputFields</b> function converts user information into a user BLOB that can be consumed by EAPHost run-time functions. 


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
The version of the EAPHost Peer APIs.

</td>
</tr>
</table>
 


### -param dwFlags [in]

A combination of <a href="https://msdn.microsoft.com/b6305349-3418-475e-8a37-2c06b399556e">EAP flags</a> that describe the  EAP authentication session behavior.


### -param dwSizeofUIContextData [in]

The size of the context data in <i>pUIContextData</i>, in bytes.


### -param pUIContextData [in]

Pointer to a BLOB that contains UI context data, represented as inner pointers to field data. These inner pointers must be freed by passing them to <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>, starting with the innermost pointer.


### -param pEapInteractiveUIData [in]

Pointer that receives an <a href="https://msdn.microsoft.com/68141611-4a1c-409e-8ed2-3d21a76640c3">EAP_INTERACTIVE_UI_DATA</a> structure that contains configuration information for interactive UI components raised on an EAP supplicant.


### -param pdwSizeOfDataFromInteractiveUI [in, out]

A pointer to a DWORD that specifies the size, in bytes, of the buffer pointed to by <i>ppDataFromInteractiveUI</i>. If this value is not set to zero, then a pointer to a buffer of the size specified in this parameter must be supplied to <i>ppDataFromInteractiveUI</i>. 


### -param ppDataFromInteractiveUI [in, out]

  Pointer that receives a credentials BLOB that can be used in authentication.
                The caller should free the inner pointers
                using the function <a href="https://msdn.microsoft.com/162c796c-b9dc-465a-a1bc-f11d740f3fa0">EapHostPeerFreeMemory</a>, starting at the innermost pointer. If a non-null value is supplied for this parameter (meaning that an existing data BLOB is passed to it), the supplied data BLOB will be updated and returned in this parameter. If a non-NULL BLOB value is supplied, the <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> function should be used. 


### -param ppEapError [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/6af8cb67-da77-491a-98de-df10b6b7f46d">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="https://msdn.microsoft.com/c80ac625-8202-49a7-813a-62a9e0d15058">EapHostPeerFreeErrorMemory</a>.


### -param ppvReserved [in, out]

Reserved for future use. This parameter must be set to 0.


## -remarks



<b>EapHostPeerQueryUIBlobFromInteractiveUIInputFields</b> can be employed to support Single-Sign-On (SSO). In an SSO scenario, <b>EapHostPeerQueryUIBlobFromInteractiveUIInputFields</b> is the last API to be called before resuming a regular call sequence. For more information, see <a href="https://msdn.microsoft.com/83276783-aee5-43ac-982d-1144df982a7d">Supplicant API Call Sequence</a>.




## -see-also




<a href="https://msdn.microsoft.com/92a1df11-10f9-4e55-a7ec-db026aaf5c24">EAPHost Supplicant Configuration Functions</a>



<a href="https://msdn.microsoft.com/126ef6cc-aa65-4770-b81a-82d25213618c"> SSO and PLAP</a>
 

 

