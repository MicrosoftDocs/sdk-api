---
UID: NS:tbs.tdTBS_CONTEXT_PARAMS2
title: TBS_CONTEXT_PARAMS2 (tbs.h)
description: Specifies the version of the TBS context implementation. You must use this structure if your application works with both versions of TPM.
helpviewer_keywords: ["*PTBS_CONTEXT_PARAMS2","PTBS_CONTEXT_PARAMS2","PTBS_CONTEXT_PARAMS2 structure pointer [TBS]","TBS_CONTEXT_PARAMS2","TBS_CONTEXT_PARAMS2 structure [TBS]","tbs.tbs_context_params2","tbs/PTBS_CONTEXT_PARAMS2","tbs/TBS_CONTEXT_PARAMS2"]
old-location: tbs\tbs_context_params2.htm
tech.root: TBS
ms.assetid: B113B422-A66E-4498-99DA-65D4ED0B84B1
ms.date: 12/05/2018
ms.keywords: '*PTBS_CONTEXT_PARAMS2, PTBS_CONTEXT_PARAMS2, PTBS_CONTEXT_PARAMS2 structure pointer [TBS], TBS_CONTEXT_PARAMS2, TBS_CONTEXT_PARAMS2 structure [TBS], tbs.tbs_context_params2, tbs/PTBS_CONTEXT_PARAMS2, tbs/TBS_CONTEXT_PARAMS2'
req.header: tbs.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TBS_CONTEXT_PARAMS2, *PTBS_CONTEXT_PARAMS2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tdTBS_CONTEXT_PARAMS2
 - tbs/tdTBS_CONTEXT_PARAMS2
 - PTBS_CONTEXT_PARAMS2
 - tbs/PTBS_CONTEXT_PARAMS2
 - TBS_CONTEXT_PARAMS2
 - tbs/TBS_CONTEXT_PARAMS2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tbs.h
api_name:
 - TBS_CONTEXT_PARAMS2
---

# TBS_CONTEXT_PARAMS2 structure


## -description

Specifies the version of the TBS context implementation. You must use this structure if your application works with both versions of TPM.

Applications interacting with just TPM 2.0 should pass a pointer to a <b>TBS_CONTEXT_PARAMS2</b> structure, with  <b>version</b> set to TPM_VERSION_20, and <b>includeTpm20</b> set to 1. 

Applications interacting with both TPM 1.2 and TPM 2.0 should pass a pointer to a <b>TBS_CONTEXT_PARAMS2</b> structure, with  <b>version</b> set to TPM_VERSION_20, <b>includeTpm20</b> set to 1, and <b>includeTpm12</b> set to 1.

## -struct-fields

### -field version

The version of the TBS context implementation. This must be set to 	TPM_VERSION_20.

### -field requestRaw

### -field includeTpm12

### -field includeTpm20

### -field asUINT32

Used to access all of the  bits in one variable.

### -field includeTpm12:1

Set to 1 if the TBS commands are to work on TPM 1.2.

### -field includeTpm20:1

Set to 1 if the TBS commands are to work on TPM 2.0.

### -field requestRaw:1

Set to 1 to request raw content.

