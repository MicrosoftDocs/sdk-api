---
UID: NS:tbs.tdTBS_CONTEXT_PARAMS
title: tdTBS_CONTEXT_PARAMS
author: windows-sdk-content
description: Specifies the version of the TBS context implementation.
old-location: tbs\tbs_context_params.htm
old-project: tbs
ms.assetid: 1b2093b3-6e5e-4289-9b1b-48027ded0fac
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PTBS_CONTEXT_PARAMS, TBS_CONTEXT_PARAMS, TBS_CONTEXT_PARAMS structure [TBS], tbs.tbs_context_params, tbs/TBS_CONTEXT_PARAMS, tdTBS_CONTEXT_PARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: TBS_CONTEXT_PARAMS, *PTBS_CONTEXT_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tbs.h
api_name:
 - TBS_CONTEXT_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# tdTBS_CONTEXT_PARAMS structure


## -description


Specifies the version of the TBS context implementation.

To connect to TBS, the client must run as administrator. TBS also limits access to locality ZERO.


## -struct-fields




### -field version

The version of the TBS context implementation. This parameter must be TBS_CONTEXT_VERSION_ONE.

