---
UID: NS:wincrypt._CERT_LOGOTYPE_DATA
title: CERT_LOGOTYPE_DATA (wincrypt.h)
description: Contains logotype data.
helpviewer_keywords: ["*PCERT_LOGOTYPE_DATA","CERT_LOGOTYPE_DATA","CERT_LOGOTYPE_DATA structure [Security]","PCERT_LOGOTYPE_DATA","PCERT_LOGOTYPE_DATA structure pointer [Security]","security.cert_logotype_data","wincrypt/CERT_LOGOTYPE_DATA","wincrypt/PCERT_LOGOTYPE_DATA"]
old-location: security\cert_logotype_data.htm
tech.root: security
ms.assetid: f170dd48-a0f4-45e0-b5b8-a5f446d1a86e
ms.date: 12/05/2018
ms.keywords: '*PCERT_LOGOTYPE_DATA, CERT_LOGOTYPE_DATA, CERT_LOGOTYPE_DATA structure [Security], PCERT_LOGOTYPE_DATA, PCERT_LOGOTYPE_DATA structure pointer [Security], security.cert_logotype_data, wincrypt/CERT_LOGOTYPE_DATA, wincrypt/PCERT_LOGOTYPE_DATA'
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
req.typenames: CERT_LOGOTYPE_DATA, *PCERT_LOGOTYPE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_LOGOTYPE_DATA
 - wincrypt/_CERT_LOGOTYPE_DATA
 - PCERT_LOGOTYPE_DATA
 - wincrypt/PCERT_LOGOTYPE_DATA
 - CERT_LOGOTYPE_DATA
 - wincrypt/CERT_LOGOTYPE_DATA
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
 - CERT_LOGOTYPE_DATA
---

# CERT_LOGOTYPE_DATA structure


## -description

The <b>CERT_LOGOTYPE_DATA</b> structure contains logotype data.

## -struct-fields

### -field cLogotypeImage

The number of elements in the <b>rgLogotypeImage</b> array.

### -field rgLogotypeImage

An array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_image">CERT_LOGOTYPE_IMAGE</a> structures that contain the logotype images. The <b>cLogotypeImage</b> member contains the number of elements in this array.

### -field cLogotypeAudio

The number of elements in the <b>rgLogotypeAudio</b> array.

### -field rgLogotypeAudio

An array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_audio">CERT_LOGOTYPE_AUDIO</a> structures that contain the logotype audio clips. The <b>cLogotypeAudio</b> member contains the number of elements in this array.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_info">CERT_LOGOTYPE_INFO</a>