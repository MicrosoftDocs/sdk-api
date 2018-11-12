---
UID: NS:capi._JAVA_TRUST
title: "_JAVA_TRUST"
author: windows-sdk-content
description: Contains trust information.
old-location: winprog\java_trust.htm
tech.root: devnotes
ms.assetid: ceb8cfc4-3b29-47d1-a651-d3cee898c1eb
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PJAVA_TRUST, JAVA_TRUST, JAVA_TRUST structure [Windows API], PJAVA_TRUST, PJAVA_TRUST structure pointer [Windows API], _JAVA_TRUST, capi/JAVA_TRUST, capi/PJAVA_TRUST, winprog.java_trust"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: capi.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Capi.h
api_name:
 - JAVA_TRUST
product: Windows
targetos: Windows
req.typenames: JAVA_TRUST, *PJAVA_TRUST
req.redist: 
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
 

 

