---
UID: NS:wincrypt._CERT_LOGOTYPE_REFERENCE
title: "_CERT_LOGOTYPE_REFERENCE"
author: windows-sdk-content
description: Contains logotype reference information.
old-location: security\cert_logotype_reference.htm
tech.root: seccrypto
ms.assetid: 22e6492e-afc2-4160-ad6c-0b65265eafeb
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: "*PCERT_LOGOTYPE_REFERENCE, CERT_LOGOTYPE_REFERENCE, CERT_LOGOTYPE_REFERENCE structure [Security], PCERT_LOGOTYPE_REFERENCE, PCERT_LOGOTYPE_REFERENCE structure pointer [Security], _CERT_LOGOTYPE_REFERENCE, security.cert_logotype_reference, wincrypt/CERT_LOGOTYPE_REFERENCE, wincrypt/PCERT_LOGOTYPE_REFERENCE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
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
 - Wincrypt.h
api_name:
 - CERT_LOGOTYPE_REFERENCE
product: Windows
targetos: Windows
req.typenames: CERT_LOGOTYPE_REFERENCE, *PCERT_LOGOTYPE_REFERENCE
req.redist: 
---

# _CERT_LOGOTYPE_REFERENCE structure


## -description


The <b>CERT_LOGOTYPE_REFERENCE</b> structure contains logotype reference information.


## -struct-fields




### -field cHashedUrl

The number of elements in the <b>rgHashedUrl</b> array.


### -field rgHashedUrl

An array of <a href="https://msdn.microsoft.com/961feb88-b924-4834-bc68-d87f410259f1">CERT_HASHED_URL</a> structures that contain the hashed URL of the logotype. The <b>cHashedUrl</b> member contains the number of elements in this array.

