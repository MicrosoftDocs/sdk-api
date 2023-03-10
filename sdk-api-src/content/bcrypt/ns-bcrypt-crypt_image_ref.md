---
UID: NS:bcrypt._CRYPT_IMAGE_REF
title: CRYPT_IMAGE_REF (bcrypt.h)
description: Contains information about a CNG provider module.
helpviewer_keywords: ["*PCRYPT_IMAGE_REF","CRYPT_IMAGE_REF","CRYPT_IMAGE_REF structure [Security]","CRYPT_MIN_DEPENDENCIES","CRYPT_PROCESS_ISOLATE","PCRYPT_IMAGE_REF","PCRYPT_IMAGE_REF structure pointer [Security]","bcrypt/CRYPT_IMAGE_REF","bcrypt/PCRYPT_IMAGE_REF","security.crypt_image_ref"]
old-location: security\crypt_image_ref.htm
tech.root: security
ms.assetid: fb853879-3ee9-45e7-bab6-31f8f8211680
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_IMAGE_REF, CRYPT_IMAGE_REF, CRYPT_IMAGE_REF structure [Security], CRYPT_MIN_DEPENDENCIES, CRYPT_PROCESS_ISOLATE, PCRYPT_IMAGE_REF, PCRYPT_IMAGE_REF structure pointer [Security], bcrypt/CRYPT_IMAGE_REF, bcrypt/PCRYPT_IMAGE_REF, security.crypt_image_ref'
req.header: bcrypt.h
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
req.typenames: CRYPT_IMAGE_REF, *PCRYPT_IMAGE_REF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_IMAGE_REF
 - bcrypt/_CRYPT_IMAGE_REF
 - PCRYPT_IMAGE_REF
 - bcrypt/PCRYPT_IMAGE_REF
 - CRYPT_IMAGE_REF
 - bcrypt/CRYPT_IMAGE_REF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Bcrypt.h
api_name:
 - CRYPT_IMAGE_REF
---

# CRYPT_IMAGE_REF structure


## -description

The <b>CRYPT_IMAGE_REF</b> structure contains information about a CNG provider module.

## -struct-fields

### -field pszImage

A pointer to a null-terminated Unicode string that contains the name of the provider module.

### -field dwFlags

A set of flags that indicate how CNG will manage the binary image with respect to this interface. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_MIN_DEPENDENCIES"></a><a id="crypt_min_dependencies"></a><dl>
<dt><b>CRYPT_MIN_DEPENDENCIES</b></dt>
</dl>
</td>
<td width="60%">
The provider for this interface is only dependent on a minimum set of system components.  This flag applies to a specific interface only and does not mean that all interfaces supported by the binary image conform to this standard.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_PROCESS_ISOLATE"></a><a id="crypt_process_isolate"></a><dl>
<dt><b>CRYPT_PROCESS_ISOLATE</b></dt>
</dl>
</td>
<td width="60%">
This flag is not used.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptresolveproviders">BCryptResolveProviders</a>



<a href="/windows/desktop/api/bcrypt/ns-bcrypt-crypt_provider_ref">CRYPT_PROVIDER_REF</a>