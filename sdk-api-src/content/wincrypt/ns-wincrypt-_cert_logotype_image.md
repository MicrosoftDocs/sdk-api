---
UID: NS:wincrypt._CERT_LOGOTYPE_IMAGE
title: "_CERT_LOGOTYPE_IMAGE"
author: windows-sdk-content
description: Contains information about an image logotype.
old-location: security\cert_logotype_image.htm
tech.root: seccrypto
ms.assetid: d1dff71c-41e1-4f02-93b4-019d688ed012
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: "*PCERT_LOGOTYPE_IMAGE, CERT_LOGOTYPE_IMAGE, CERT_LOGOTYPE_IMAGE structure [Security], PCERT_LOGOTYPE_IMAGE, PCERT_LOGOTYPE_IMAGE structure pointer [Security], _CERT_LOGOTYPE_IMAGE, security.cert_logotype_image, wincrypt/CERT_LOGOTYPE_IMAGE, wincrypt/PCERT_LOGOTYPE_IMAGE"
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
 - CERT_LOGOTYPE_IMAGE
product: Windows
targetos: Windows
req.typenames: CERT_LOGOTYPE_IMAGE, *PCERT_LOGOTYPE_IMAGE
req.redist: 
---

# _CERT_LOGOTYPE_IMAGE structure


## -description


The <b>CERT_LOGOTYPE_IMAGE</b> structure contains information about an image logotype.


## -struct-fields




### -field LogotypeDetails

A <a href="https://msdn.microsoft.com/cde420a8-c755-4c45-ab81-4897b08d9dd6">CERT_LOGOTYPE_DETAILS</a> structure that contains additional information about the image.


### -field pLogotypeImageInfo

The address of a <a href="https://msdn.microsoft.com/d7116e54-dbf2-457e-8d33-1c0fd5641fe7">CERT_LOGOTYPE_IMAGE_INFO</a> structure that contains the image information.


## -see-also




<a href="https://msdn.microsoft.com/f170dd48-a0f4-45e0-b5b8-a5f446d1a86e">CERT_LOGOTYPE_DATA</a>
 

 

