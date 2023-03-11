---
UID: NS:iketypes.IKEEXT_CREDENTIAL_PAIR1_
title: IKEEXT_CREDENTIAL_PAIR1 (iketypes.h)
description: Is used to store credential information used for the authentication. (IKEEXT_CREDENTIAL_PAIR1)
helpviewer_keywords: ["IKEEXT_CREDENTIAL_PAIR1","IKEEXT_CREDENTIAL_PAIR1 structure [Filtering]","fwp.ikeext_credential_pair1","iketypes/IKEEXT_CREDENTIAL_PAIR1"]
old-location: fwp\ikeext_credential_pair1.htm
tech.root: fwp
ms.assetid: fe18503d-fd1c-45b6-86c7-9b452036f8c8
ms.date: 12/05/2018
ms.keywords: IKEEXT_CREDENTIAL_PAIR1, IKEEXT_CREDENTIAL_PAIR1 structure [Filtering], fwp.ikeext_credential_pair1, iketypes/IKEEXT_CREDENTIAL_PAIR1
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
req.typenames: IKEEXT_CREDENTIAL_PAIR1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CREDENTIAL_PAIR1_
 - iketypes/IKEEXT_CREDENTIAL_PAIR1_
 - IKEEXT_CREDENTIAL_PAIR1
 - iketypes/IKEEXT_CREDENTIAL_PAIR1
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
 - IKEEXT_CREDENTIAL_PAIR1
---

# IKEEXT_CREDENTIAL_PAIR1 structure


## -description

The <b>IKEEXT_CREDENTIAL_PAIR1</b> structure is  used to store credential information used for the authentication.
[IKEEXT_CREDENTIAL_PAIR2](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair2) is available. For Windows Vista, [IKEEXT_CREDENTIAL_PAIR0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair0) is available.</div><div> </div>

## -struct-fields

### -field localCredentials

Local credentials used for authentication.

See [IKEEXT_CREDENTIAL1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential1) for more information.

### -field peerCredentials

Peer credentials used for authentication.

See [IKEEXT_CREDENTIAL1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential1) for more information.

## -see-also

[IKEEXT_CREDENTIAL1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential1)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
