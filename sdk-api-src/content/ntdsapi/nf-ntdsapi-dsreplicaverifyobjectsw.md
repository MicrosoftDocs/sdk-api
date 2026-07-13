---
UID: NF:ntdsapi.DsReplicaVerifyObjectsW
title: DsReplicaVerifyObjectsW function (ntdsapi.h)
description: Verifies all objects for a naming context with a source. (Unicode)
helpviewer_keywords: ["DS_EXIST_ADVISORY_MODE", "DsReplicaVerifyObjects", "DsReplicaVerifyObjects function [Active Directory]", "DsReplicaVerifyObjectsW", "ad.dsreplicaverifyobjects", "ntdsapi/DsReplicaVerifyObjects", "ntdsapi/DsReplicaVerifyObjectsW"]
old-location: ad\dsreplicaverifyobjects.htm
tech.root: ad
ms.assetid: d0e139dc-6aaf-47e1-a76f-4e84f17aa7c6
ms.date: 12/05/2018
ms.keywords: DS_EXIST_ADVISORY_MODE, DsReplicaVerifyObjects, DsReplicaVerifyObjects function [Active Directory], DsReplicaVerifyObjectsA, DsReplicaVerifyObjectsW, ad.dsreplicaverifyobjects, ntdsapi/DsReplicaVerifyObjects, ntdsapi/DsReplicaVerifyObjectsA, ntdsapi/DsReplicaVerifyObjectsW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsReplicaVerifyObjectsW (Unicode) and DsReplicaVerifyObjectsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsReplicaVerifyObjectsW
 - ntdsapi/DsReplicaVerifyObjectsW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsReplicaVerifyObjects
 - DsReplicaVerifyObjectsA
 - DsReplicaVerifyObjectsW
---

# DsReplicaVerifyObjectsW function


## -description

The <b>DsReplicaVerifyObjects</b> function verifies all objects for a naming context with a source.

## -parameters

### -param hDS [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a>, 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a>, or <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithspna">DsBindWithSpn</a> function.

### -param NameContext [in]

Pointer to a null-terminated string that contains the distinguished name of the naming context.

### -param pUuidDsaSrc [in]

Pointer to a <b>UUID</b> value that contains the <b>objectGuid</b> of the directory system agent object.

### -param ulOptions [in]

Contains a set of flags that modify the behavior of the function. This can be zero or the following value.



#### DS_EXIST_ADVISORY_MODE

Do not delete objects in response to  this function.


##### - ulOptions.DS_EXIST_ADVISORY_MODE

Do not delete objects in response to  this function.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 error otherwise. Possible error values include the following.

## -see-also

<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithspna">DsBindWithSpn</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsReplicaVerifyObjects as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
