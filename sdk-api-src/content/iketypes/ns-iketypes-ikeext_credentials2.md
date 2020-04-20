---
UID: NS:iketypes.IKEEXT_CREDENTIALS2_
title: IKEEXT_CREDENTIALS2 (iketypes.h)
description: Is used to store multiple credential pairs.helpviewer_keywords: ["IKEEXT_CREDENTIALS2","IKEEXT_CREDENTIALS2 structure [Filtering]","fwp.ikeext_credentials2","iketypes/IKEEXT_CREDENTIALS2"]
old-location: fwp\ikeext_credentials2.htm
tech.root: fwp
ms.assetid: 4099b6e7-0b3b-40ea-821c-3ff28a6f788f
ms.date: 12/05/2018
ms.keywords: IKEEXT_CREDENTIALS2, IKEEXT_CREDENTIALS2 structure [Filtering], fwp.ikeext_credentials2, iketypes/IKEEXT_CREDENTIALS2
f1_keywords:
- iketypes/IKEEXT_CREDENTIALS2
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
- IKEEXT_CREDENTIALS2
targetos: Windows
req.typenames: IKEEXT_CREDENTIALS2
req.redist: 
ms.custom: 19H1
---

# IKEEXT_CREDENTIALS2 structure


## -description


The <b>IKEEXT_CREDENTIALS2</b> structure is used to store multiple credential pairs.
[IKEEXT_CREDENTIALS1](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credentials1)a> is available. For Windows Vista, [IKEEXT_CREDENTIALS0](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credentials0)a>  is available.</div><div> </div>

## -struct-fields




### -field numCredentials

Type: <b>UINT32</b>

Number of [IKEEXT_CREDENTIAL_PAIR2](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair2)a> structures in the array.


### -field credentials

Type: [IKEEXT_CREDENTIAL_PAIR2](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair2)a>*</b>

[size_is(numCredentials)]

Pointer to an array of [IKEEXT_CREDENTIAL_PAIR2](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair2)a> structures.


## -remarks



IKE and IKEv2 have only 1 pair.

AuthIP
has 1 pair, or 2 pairs if EM was enabled.

MM authentication is always index 0.

EM authentication, if it occurs,
is index 1.




## -see-also




[IKEEXT_CREDENTIAL_PAIR2](https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_credential_pair2)a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

