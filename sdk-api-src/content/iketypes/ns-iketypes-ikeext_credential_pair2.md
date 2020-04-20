---
UID: NS:iketypes.IKEEXT_CREDENTIAL_PAIR2_
title: IKEEXT_CREDENTIAL_PAIR2 (iketypes.h)
description: Is used to store credential information used for the authentication.helpviewer_keywords: ["IKEEXT_CREDENTIAL_PAIR2","IKEEXT_CREDENTIAL_PAIR2 structure [Filtering]","fwp.ikeext_credential_pair2","iketypes/IKEEXT_CREDENTIAL_PAIR2"]
old-location: fwp\ikeext_credential_pair2.htm
tech.root: fwp
ms.assetid: 013b7b6c-aee6-40f3-b8c4-ef98784165ca
ms.date: 12/05/2018
ms.keywords: IKEEXT_CREDENTIAL_PAIR2, IKEEXT_CREDENTIAL_PAIR2 structure [Filtering], fwp.ikeext_credential_pair2, iketypes/IKEEXT_CREDENTIAL_PAIR2
f1_keywords:
- iketypes/IKEEXT_CREDENTIAL_PAIR2
dev_langs:
- c++
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- iketypes.h
api_name:
- IKEEXT_CREDENTIAL_PAIR2
targetos: Windows
req.typenames: IKEEXT_CREDENTIAL_PAIR2
req.redist: 
ms.custom: 19H1
---

# IKEEXT_CREDENTIAL_PAIR2 structure


## -description


The <b>IKEEXT_CREDENTIAL_PAIR2</b> structure is  used to store credential information used for the authentication.
[IKEEXT_CREDENTIAL_PAIR1](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair1)a> is available. For Windows Vista, [IKEEXT_CREDENTIAL_PAIR0](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair0)a>  is available.</div><div> </div>

## -struct-fields




### -field localCredentials

Type: [IKEEXT_CREDENTIAL2](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential2)a></b>

Local credentials used for authentication.


### -field peerCredentials

Type: [IKEEXT_CREDENTIAL2](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential2)a></b>

Peer credentials used for authentication.


## -see-also




[IKEEXT_CREDENTIAL2](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential2)a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

