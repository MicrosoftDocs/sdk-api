---
UID: NF:combaseapi.CoRegisterActivationFilter
title: CoRegisterActivationFilter function (combaseapi.h)
description: Registers a process-wide filter to process activation requests.
helpviewer_keywords: ["CoRegisterActivationFilter","CoRegisterActivationFilter function [COM]","com.coregisteractivationfilter","combaseapi/CoRegisterActivationFilter"]
old-location: com\coregisteractivationfilter.htm
tech.root: com
ms.assetid: 4189633F-9B14-4EAD-84BD-F74355376164
ms.date: 12/05/2018
ms.keywords: CoRegisterActivationFilter, CoRegisterActivationFilter function [COM], com.coregisteractivationfilter, combaseapi/CoRegisterActivationFilter
req.header: combaseapi.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoRegisterActivationFilter
 - combaseapi/CoRegisterActivationFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - api-ms-win-core-com-l1-1-1.dll
 - Ole32.dll
 - ComBase.dll
api_name:
 - CoRegisterActivationFilter
---

# CoRegisterActivationFilter function


## -description

Registers a process-wide filter to process activation requests.

## -parameters

### -param pActivationFilter [in]

Pointer to the filter to register.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This registers one and only one process-wide filter.

