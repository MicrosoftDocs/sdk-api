---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WINTRUST_SIGNATURE_SETTINGS_ structure


## -description


The <b>WINTRUST_SIGNATURE_SETTINGS</b> structure can be used to specify the signatures on a file.


## -struct-fields




### -field cbStruct

Size, in bytes, of this structure.


### -field dwIndex

Contains the index of the signature to be validated if the <b>dwFlags</b> member is set to <b>WSS_VERIFY_SPECIFIC</b>.


### -field dwFlags

Flags that can be used to refine behavior. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WSS_VERIFY_SPECIFIC"></a><a id="wss_verify_specific"></a><dl>
<dt><b>WSS_VERIFY_SPECIFIC</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Set this value if you set the <b>dwIndex</b> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="WSS_GET_SECONDARY_SIG_COUNT"></a><a id="wss_get_secondary_sig_count"></a><dl>
<dt><b>WSS_GET_SECONDARY_SIG_COUNT</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Set this value to return the number of secondary signatures found in the <b>cSecondarySigs</b> member.

</td>
</tr>
</table>
 


### -field cSecondarySigs

Contains the number of secondary signatures found if the <b>dwFlags</b> member is set to <b>WSS_GET_SECONDARY_SIG_COUNT</b>.


### -field dwVerifiedSigIndex

The index used for verification. This member is set on return from Wintrust.


### -field pCryptoPolicy

Pointer to a <a href="https://msdn.microsoft.com/12D9F82C-F484-43B0-BD55-F07321058671">CERT_STRONG_SIGN_PARA</a> structure that contains the policy that a signature must pass to be considered valid.


## -see-also




<a href="https://msdn.microsoft.com/12D9F82C-F484-43B0-BD55-F07321058671">CERT_STRONG_SIGN_PARA</a>



<a href="https://msdn.microsoft.com/b7efac6a-ac9f-477a-aada-63fe32208e6f">WinVerifyTrust</a>
 

 

