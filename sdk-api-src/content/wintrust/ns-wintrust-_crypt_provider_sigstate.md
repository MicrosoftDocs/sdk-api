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

# _CRYPT_PROVIDER_SIGSTATE structure


## -description


The <b>CRYPT_PROVIDER_SIGSTATE</b> structure is used to communicate between policy providers and Wintrust.


## -struct-fields




### -field cbStruct

Size, in bytes, of this structure.


### -field rhSecondarySigs

Pointer to an array of secondary signature handles.


### -field hPrimarySig

Handle of the primary signature.


### -field fFirstAttemptMade

Specifies whether the first attempt to verify a signature has been made.


### -field fNoMoreSigs

Specifies whether there exist further signatures that await verification.


### -field cSecondarySigs

Number of secondary signatures.


### -field dwCurrentIndex

Index of the signature currently being verified.


### -field fSupportMultiSig

Specifies whether the policy provider supports multiple signatures.


### -field dwCryptoPolicySupport

Identifies the portion of the policy provider that  supports cryptographic policy. This can be one of the following values:

<ul>
<li>WSS_OBJTRUST_SUPPORT</li>
<li>WSS_SIGTRUST_SUPPORT</li>
<li>WSS_CERTTRUST_SUPPORT</li>
</ul>

### -field iAttemptCount

 


### -field fCheckedSealing

 


### -field pSealingSignature

 




## -see-also




<a href="https://msdn.microsoft.com/E0F526B4-AFDE-4481-B49F-EE7467F97A46">WINTRUST_SIGNATURE_SETTINGS</a>
 

 

