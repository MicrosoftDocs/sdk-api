---
UID: NS:wincrypt._CERT_LOGOTYPE_DETAILS
title: CERT_LOGOTYPE_DETAILS (wincrypt.h)
author: windows-sdk-content
description: Contains additional information about a logotype.
old-location: security\cert_logotype_details.htm
tech.root: SecCrypto
ms.assetid: cde420a8-c755-4c45-ab81-4897b08d9dd6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PCERT_LOGOTYPE_DETAILS, CERT_LOGOTYPE_DETAILS, CERT_LOGOTYPE_DETAILS structure [Security], PCERT_LOGOTYPE_DETAILS, PCERT_LOGOTYPE_DETAILS structure pointer [Security], security.cert_logotype_details, wincrypt/CERT_LOGOTYPE_DETAILS, wincrypt/PCERT_LOGOTYPE_DETAILS"
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
ms.custom: 19H1
---

# CERT_LOGOTYPE_DETAILS structure


## -description


The <b>CERT_LOGOTYPE_DETAILS</b> structure contains additional information about a logotype.


## -struct-fields




### -field pwszMimeType

The address of a null-terminated Unicode string that contains the Multipurpose Internet Mail Extensions (MIME) type of the logotype.


### -field cHashedUrl

The number of elements in the <b>rgHashedUrl</b> array.


### -field rgHashedUrl

An array of <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_hashed_url">CERT_HASHED_URL</a> structures that contain the hashed URLs of the logotype. The <b>cHashedUrl</b> member contains the number of elements in this array.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_logotype_audio">CERT_LOGOTYPE_AUDIO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_logotype_image">CERT_LOGOTYPE_IMAGE</a>
 

 

