---
UID: NS:wincrypt._CERT_LOGOTYPE_IMAGE
title: CERT_LOGOTYPE_IMAGE (wincrypt.h)
description: Contains information about an image logotype.
helpviewer_keywords: ["*PCERT_LOGOTYPE_IMAGE","CERT_LOGOTYPE_IMAGE","CERT_LOGOTYPE_IMAGE structure [Security]","PCERT_LOGOTYPE_IMAGE","PCERT_LOGOTYPE_IMAGE structure pointer [Security]","security.cert_logotype_image","wincrypt/CERT_LOGOTYPE_IMAGE","wincrypt/PCERT_LOGOTYPE_IMAGE"]
old-location: security\cert_logotype_image.htm
tech.root: security
ms.assetid: d1dff71c-41e1-4f02-93b4-019d688ed012
ms.date: 12/05/2018
ms.keywords: '*PCERT_LOGOTYPE_IMAGE, CERT_LOGOTYPE_IMAGE, CERT_LOGOTYPE_IMAGE structure [Security], PCERT_LOGOTYPE_IMAGE, PCERT_LOGOTYPE_IMAGE structure pointer [Security], security.cert_logotype_image, wincrypt/CERT_LOGOTYPE_IMAGE, wincrypt/PCERT_LOGOTYPE_IMAGE'
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
targetos: Windows
req.typenames: CERT_LOGOTYPE_IMAGE, *PCERT_LOGOTYPE_IMAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_LOGOTYPE_IMAGE
 - wincrypt/_CERT_LOGOTYPE_IMAGE
 - PCERT_LOGOTYPE_IMAGE
 - wincrypt/PCERT_LOGOTYPE_IMAGE
 - CERT_LOGOTYPE_IMAGE
 - wincrypt/CERT_LOGOTYPE_IMAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_LOGOTYPE_IMAGE
---

# CERT_LOGOTYPE_IMAGE structure


## -description

The <b>CERT_LOGOTYPE_IMAGE</b> structure contains information about an image logotype.

## -struct-fields

### -field LogotypeDetails

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_details">CERT_LOGOTYPE_DETAILS</a> structure that contains additional information about the image.

### -field pLogotypeImageInfo

The address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_image_info">CERT_LOGOTYPE_IMAGE_INFO</a> structure that contains the image information.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_data">CERT_LOGOTYPE_DATA</a>