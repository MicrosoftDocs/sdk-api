---
UID: NF:tdh.TdhUnloadManifestFromMemory
tech.root: ETW
title: TdhUnloadManifestFromMemory (tdh.h)
ms.date: 12/05/2022
ms.keywords: TdhUnloadManifestFromMemory
targetos: Windows
description: Unloads the manifest from memory.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: tdh.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1903 [desktop apps only]
req.target-min-winversvr: Windows Server 2019 [desktop apps only]
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-eventing-tdh-l1-1-2.dll
 - api-ms-win-eventing-tdh-l1-1-1.dll
 - tdh.h
api_name:
 - TdhUnloadManifestFromMemory
f1_keywords:
 - TdhUnloadManifestFromMemory
 - tdh/TdhUnloadManifestFromMemory
dev_langs:
 - c++
helpviewer_keywords:
 - TdhUnloadManifestFromMemory
---

# TdhUnloadManifestFromMemory function (tdh.h)

## -description

Unloads the manifest from memory.

## -parameters

### -param pData [in]

Type: **const void***

Pointer to the data to be stored.

### -param cbData [in]

Type: **ULONG**

Size of the data in the buffer pointed to by *pData*, in bytes.

## -returns

Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

| Return code | Description |
| -- | -- |
| **ERROR_INVALID_PARAMETER** | One or more of the parameters is not valid. |
| **ERROR_FILE_NOT_FOUND** | The file pointed to by *pData* was not found. |
| **ERROR_NOT_ENOUGH_MEMORY** | Memory allocations failed. |
| **ERROR_RESOURCE_NOT_FOUND** | The file does not contain any eventing metadata resources. |

## -remarks

## -see-also
