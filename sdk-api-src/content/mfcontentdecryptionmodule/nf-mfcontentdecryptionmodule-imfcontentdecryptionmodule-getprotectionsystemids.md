---
UID: NF:mfcontentdecryptionmodule.IMFContentDecryptionModule.GetProtectionSystemIds
title: IMFContentDecryptionModule::GetProtectionSystemIds
ms.date: 08/05/2022
targetos: Windows
description: The IMFContentDecryptionModule::GetProtectionSystemIds gets a list of SystemIDs that the IMFContentDecryptionModule supports. 
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfcontentdecryptionmodule.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfcontentdecryptionmodule.h
api_name:
 - IMFContentDecryptionModule::GetProtectionSystemIds
f1_keywords:
 - IMFContentDecryptionModule::GetProtectionSystemIds
 - mfcontentdecryptionmodule/IMFContentDecryptionModule::GetProtectionSystemIds
dev_langs:
 - c++
---

## -description

Gets a list of **SystemIDs** that the **IMFContentDecryptionModule** supports.

## -parameters

### -param systemIds

A **GUID** array in which the SystemIDs are returned.

### -param count

The count of SystemIDs returned in the *systemIds* parameter.

## -returns

Returns S_OK on success.

## -remarks

**SystemIDs** are identifiers used in the "cenc" Initialization Data Format. For more details, see ["cenc" Initialization Data Format](https://w3c.github.io/encrypted-media/format-registry/initdata/cenc.html).

The *systemIds* memory must be allocated and freed using [CoTaskMem](../combaseapi/nf-combaseapi-cotaskmemalloc.md).

## -see-also