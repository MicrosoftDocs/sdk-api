---
UID: NF:comsvcs.ICOMLBArguments.GetMachineName
title: ICOMLBArguments::GetMachineName (comsvcs.h)
description: Retrieves the computer name for the load balancing server.
helpviewer_keywords: ["GetMachineName","GetMachineName method [COM+]","GetMachineName method [COM+]","ICOMLBArguments interface","ICOMLBArguments interface [COM+]","GetMachineName method","ICOMLBArguments.GetMachineName","ICOMLBArguments::GetMachineName","_cos_ICOMLBArguments_GetMachineName","comsvcs/ICOMLBArguments::GetMachineName","cos.icomlbarguments_getmachinename"]
old-location: cos\icomlbarguments_getmachinename.htm
tech.root: cos
ms.assetid: b1f6adc8-2e89-4f64-9694-2342c967a142
ms.date: 12/05/2018
ms.keywords: GetMachineName, GetMachineName method [COM+], GetMachineName method [COM+],ICOMLBArguments interface, ICOMLBArguments interface [COM+],GetMachineName method, ICOMLBArguments.GetMachineName, ICOMLBArguments::GetMachineName, _cos_ICOMLBArguments_GetMachineName, comsvcs/ICOMLBArguments::GetMachineName, cos.icomlbarguments_getmachinename
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICOMLBArguments::GetMachineName
 - comsvcs/ICOMLBArguments::GetMachineName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICOMLBArguments.GetMachineName
---

# ICOMLBArguments::GetMachineName


## -description

Retrieves the computer name for the load balancing server.

## -parameters

### -param cchSvr [in]

The object's machine name.

### -param szServerName [out]

The object's server name.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomlbarguments">ICOMLBArguments</a>