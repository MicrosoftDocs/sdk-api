---
UID: NS:tbs.tdTBS_CONTEXT_PARAMS
title: TBS_CONTEXT_PARAMS (tbs.h)
description: Specifies the version of the TBS context implementation.
helpviewer_keywords: ["*PTBS_CONTEXT_PARAMS","TBS_CONTEXT_PARAMS","TBS_CONTEXT_PARAMS structure [TBS]","tbs.tbs_context_params","tbs/TBS_CONTEXT_PARAMS"]
old-location: tbs\tbs_context_params.htm
tech.root: TBS
ms.assetid: 1b2093b3-6e5e-4289-9b1b-48027ded0fac
ms.date: 12/05/2018
ms.keywords: '*PTBS_CONTEXT_PARAMS, TBS_CONTEXT_PARAMS, TBS_CONTEXT_PARAMS structure [TBS], tbs.tbs_context_params, tbs/TBS_CONTEXT_PARAMS'
req.header: tbs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: TBS_CONTEXT_PARAMS, *PTBS_CONTEXT_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tdTBS_CONTEXT_PARAMS
 - tbs/tdTBS_CONTEXT_PARAMS
 - PTBS_CONTEXT_PARAMS
 - tbs/PTBS_CONTEXT_PARAMS
 - TBS_CONTEXT_PARAMS
 - tbs/TBS_CONTEXT_PARAMS
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
 - TBS_CONTEXT_PARAMS
---

# TBS_CONTEXT_PARAMS structure


## -description

Specifies the version of the TBS context implementation.

To connect to TBS, the client must run as administrator. TBS also limits access to locality ZERO.

## -struct-fields

### -field version

The version of the TBS context implementation. This parameter must be TBS_CONTEXT_VERSION_ONE.

