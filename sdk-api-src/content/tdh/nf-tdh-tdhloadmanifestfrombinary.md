---
UID: NF:tdh.TdhLoadManifestFromBinary
title: TdhLoadManifestFromBinary function (tdh.h)
description: Takes a NULL-terminated path to a binary file that contains metadata resources needed to decode a specific event provider.
helpviewer_keywords: ["TdhLoadManifestFromBinary","TdhLoadManifestFromBinary function [ETW]","etw.tdhloadmanifestfrombinary","tdh/TdhLoadManifestFromBinary"]
old-location: etw\tdhloadmanifestfrombinary.htm
tech.root: ETW
ms.assetid: e152d25c-bbc9-4573-9575-9cf9583433a7
ms.date: 12/05/2018
ms.keywords: TdhLoadManifestFromBinary, TdhLoadManifestFromBinary function [ETW], etw.tdhloadmanifestfrombinary, tdh/TdhLoadManifestFromBinary
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TdhLoadManifestFromBinary
 - tdh/TdhLoadManifestFromBinary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tdh.dll
 - Ext-MS-Win-Eventing-Tdh-Ext-L1-1-0.dll
api_name:
 - TdhLoadManifestFromBinary
---

# TdhLoadManifestFromBinary function


## -description

Takes a NULL-terminated path to a binary file that contains metadata resources needed to decode a specific event provider.

## -parameters

### -param BinaryPath [in]

Type: <b>PWSTR</b>

Path to the ETW provider binary that contains the metadata resources.

## -returns

Type: <b>ULONG</b>

Returns ERROR_SUCCESS if successful. Otherwise, this function returns one of the following return codes in addition to others.

| Return code | Description |
| -- | -- |
| **ERROR_INVALID_PARAMETER** | One or more of the parameters is not valid. |
| **ERROR_FILE_NOT_FOUND** | The file pointed to by *BinaryPath* was not found. |
| **ERROR_NOT_ENOUGH_MEMORY** | Memory allocations failed. |
| **ERROR_RESOURCE_NOT_FOUND** | The file does not contain any eventing metadata resources. |

## -remarks

The GUIDs
    and BinaryPath string are cached.

When metadata is 
    requested for a given event or provider, but the provider is not installed in the system, the cache
    of binaries will be searched.

