---
UID: NS:iketypes.IKEEXT_CREDENTIALS0_
title: IKEEXT_CREDENTIALS0 (iketypes.h)
description: Is used to store multiple credential pairs. (IKEEXT_CREDENTIALS0)
helpviewer_keywords: ["IKEEXT_CREDENTIALS0","IKEEXT_CREDENTIALS0 structure [Filtering]","fwp.ikeext_credentials0","iketypes/IKEEXT_CREDENTIALS0"]
old-location: fwp\ikeext_credentials0.htm
tech.root: fwp
ms.assetid: 048d0a56-5d9b-4a85-b42f-8505eb6a97a9
ms.date: 12/05/2018
ms.keywords: IKEEXT_CREDENTIALS0, IKEEXT_CREDENTIALS0 structure [Filtering], fwp.ikeext_credentials0, iketypes/IKEEXT_CREDENTIALS0
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
req.typenames: IKEEXT_CREDENTIALS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CREDENTIALS0_
 - iketypes/IKEEXT_CREDENTIALS0_
 - IKEEXT_CREDENTIALS0
 - iketypes/IKEEXT_CREDENTIALS0
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
 - IKEEXT_CREDENTIALS0
---

# IKEEXT_CREDENTIALS0 structure


## -description

The <b>IKEEXT_CREDENTIALS0</b> structure is used to store multiple credential pairs.  
[IKEEXT_CREDENTIALS1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credentials1) is available. For Windows 8, [IKEEXT_CREDENTIALS2](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credentials2) is available.</div><div> </div>

## -struct-fields

### -field numCredentials

Number of [IKEEXT_CREDENTIAL_PAIR0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair0) structures in the array.

### -field credentials

[size_is(numCredentials)]

Pointer to an array of [IKEEXT_CREDENTIAL_PAIR0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair0) structures.

## -remarks

IKE has only 1 pair.

AuthIP
has 1 pair, or 2 pairs if EM was enabled.

MM authentication is always index 0.

EM authentication, if it occurs,
is index 1.

## -see-also

[IKEEXT_CREDENTIAL_PAIR0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
