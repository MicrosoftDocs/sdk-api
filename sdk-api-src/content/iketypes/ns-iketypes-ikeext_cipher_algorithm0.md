---
UID: NS:iketypes.IKEEXT_CIPHER_ALGORITHM0_
title: IKEEXT_CIPHER_ALGORITHM0 (iketypes.h)
description: Stores information about the IKE/AuthIP encryption algorithm.
helpviewer_keywords: ["IKEEXT_CIPHER_ALGORITHM0","IKEEXT_CIPHER_ALGORITHM0 structure [Filtering]","fwp.ikeext_cipher_algorithm0","iketypes/IKEEXT_CIPHER_ALGORITHM0"]
old-location: fwp\ikeext_cipher_algorithm0.htm
tech.root: fwp
ms.assetid: 940714a3-d098-4d02-9209-fcf3b24ee4e7
ms.date: 12/05/2018
ms.keywords: IKEEXT_CIPHER_ALGORITHM0, IKEEXT_CIPHER_ALGORITHM0 structure [Filtering], fwp.ikeext_cipher_algorithm0, iketypes/IKEEXT_CIPHER_ALGORITHM0
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_CIPHER_ALGORITHM0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CIPHER_ALGORITHM0_
 - iketypes/IKEEXT_CIPHER_ALGORITHM0_
 - IKEEXT_CIPHER_ALGORITHM0
 - iketypes/IKEEXT_CIPHER_ALGORITHM0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_CIPHER_ALGORITHM0
---

# IKEEXT_CIPHER_ALGORITHM0 structure


## -description

The <b>IKEEXT_CIPHER_ALGORITHM0</b> structure stores information about the IKE/AuthIP encryption algorithm.

## -struct-fields

### -field algoIdentifier

The type of encryption algorithm.

See [IKEEXT_CIPHER_TYPE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_cipher_type) for more information.

### -field keyLen

Unused parameter, always set it to 0.

### -field rounds

Unused parameter, always set it to 0.

## -remarks

<b>IKEEXT_CIPHER_ALGORITHM0</b> is a specific implementation of IKEEXT_CIPHER_ALGORITHM. See <a href="/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.

## -see-also

[IKEEXT_CIPHER_TYPE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_cipher_type)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>