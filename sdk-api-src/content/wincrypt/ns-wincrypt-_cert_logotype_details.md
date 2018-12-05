---
UID: NS:wincrypt._CERT_LOGOTYPE_DETAILS
title: "_CERT_LOGOTYPE_DETAILS"
author: windows-sdk-content
description: Contains additional information about a logotype.
old-location: security\cert_logotype_details.htm
tech.root: seccrypto
ms.assetid: cde420a8-c755-4c45-ab81-4897b08d9dd6
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: "*PCERT_LOGOTYPE_DETAILS, CERT_LOGOTYPE_DETAILS, CERT_LOGOTYPE_DETAILS structure [Security], PCERT_LOGOTYPE_DETAILS, PCERT_LOGOTYPE_DETAILS structure pointer [Security], _CERT_LOGOTYPE_DETAILS, security.cert_logotype_details, wincrypt/CERT_LOGOTYPE_DETAILS, wincrypt/PCERT_LOGOTYPE_DETAILS"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CERT_LOGOTYPE_DETAILS
product: Windows
targetos: Windows
req.typenames: CERT_LOGOTYPE_DETAILS, *PCERT_LOGOTYPE_DETAILS
req.redist: 
---

# _CERT_LOGOTYPE_DETAILS structure


## -description


The <b>CERT_LOGOTYPE_DETAILS</b> structure contains additional information about a logotype.


## -struct-fields




### -field pwszMimeType

The address of a null-terminated Unicode string that contains the Multipurpose Internet Mail Extensions (MIME) type of the logotype.


### -field cHashedUrl

The number of elements in the <b>rgHashedUrl</b> array.


### -field rgHashedUrl

An array of <a href="https://msdn.microsoft.com/961feb88-b924-4834-bc68-d87f410259f1">CERT_HASHED_URL</a> structures that contain the hashed URLs of the logotype. The <b>cHashedUrl</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/97357faa-2720-4240-a3c3-77abdce8d86d">CERT_LOGOTYPE_AUDIO</a>



<a href="https://msdn.microsoft.com/d1dff71c-41e1-4f02-93b4-019d688ed012">CERT_LOGOTYPE_IMAGE</a>
 

 

