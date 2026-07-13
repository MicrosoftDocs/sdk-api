---
UID: NS:iketypes.IKEEXT_CREDENTIALS1_
title: IKEEXT_CREDENTIALS1 (iketypes.h)
description: Is used to store multiple credential pairs. (IKEEXT_CREDENTIALS1)
helpviewer_keywords: ["IKEEXT_CREDENTIALS1","IKEEXT_CREDENTIALS1 structure [Filtering]","fwp.ikeext_credentials1","iketypes/IKEEXT_CREDENTIALS1"]
old-location: fwp\ikeext_credentials1.htm
tech.root: fwp
ms.assetid: dbd895bd-a720-4c8e-a2e7-f5614d69922c
ms.date: 12/05/2018
ms.keywords: IKEEXT_CREDENTIALS1, IKEEXT_CREDENTIALS1 structure [Filtering], fwp.ikeext_credentials1, iketypes/IKEEXT_CREDENTIALS1
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: IKEEXT_CREDENTIALS1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CREDENTIALS1_
 - iketypes/IKEEXT_CREDENTIALS1_
 - IKEEXT_CREDENTIALS1
 - iketypes/IKEEXT_CREDENTIALS1
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
 - IKEEXT_CREDENTIALS1
---

# IKEEXT_CREDENTIALS1 structure


## -description

The <b>IKEEXT_CREDENTIALS1</b> structure is used to store multiple credential pairs.
[IKEEXT_CREDENTIALS0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credentials0) is available.</div><div> </div>

## -struct-fields

### -field numCredentials

Number of [IKEEXT_CREDENTIAL_PAIR1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair1) structures in the array.

### -field credentials

[size_is(numCredentials)]

Pointer to an array of [IKEEXT_CREDENTIAL_PAIR1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair1) structures.

## -remarks

IKE and IKEv2 have only 1 pair.

AuthIP
has 1 pair, or 2 pairs if EM was enabled.

MM authentication is always index 0.

EM authentication, if it occurs,
is index 1.

## -see-also

[IKEEXT_CREDENTIAL_PAIR1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair1)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
