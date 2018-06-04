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

# _JAVA_TRUST structure


## -description


Contains trust information.


## -struct-fields




### -field cbSize

The size of this structure, in bytes.


### -field flag

Reserved.


### -field fAllActiveXPermissions

Indicates whether all ActiveX permissions were requested.


### -field fAllPermissions

Indicates whether all Java permissions were requested.


### -field dwEncodingType

The encoding type. This member can be <b>X509_ASN_ENCODING</b> or <b>PKCS_7_ASN_ENCODING</b>.


### -field pbJavaPermissions

The encoded permission blob.


### -field cbJavaPermissions

The size of the <b>pbJavaPermissions</b> buffer, in bytes.


### -field pbSigner

The encoded signer.


### -field cbSigner

The size of the <b>pbSigner</b> buffer, in bytes.


### -field pwszZone

The zone index.


### -field guidZone

Reserved.


### -field hVerify

The authenticode policy return code.


## -see-also




<a href="https://msdn.microsoft.com/b86a8f39-73a1-4e17-ac83-9ed095de4922">DownloadJavaEX</a>



<a href="https://msdn.microsoft.com/e71e7155-5981-4227-8dc2-51a9b719aa25">JAVA_POLICY_PROVIDER</a>
 

 

