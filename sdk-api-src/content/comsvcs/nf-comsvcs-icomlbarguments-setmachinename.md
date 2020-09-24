---
UID: NF:comsvcs.ICOMLBArguments.SetMachineName
title: ICOMLBArguments::SetMachineName (comsvcs.h)
description: Sets the computer name for the load balancing server.
helpviewer_keywords: ["ICOMLBArguments interface [COM+]","SetMachineName method","ICOMLBArguments.SetMachineName","ICOMLBArguments::SetMachineName","SetMachineName","SetMachineName method [COM+]","SetMachineName method [COM+]","ICOMLBArguments interface","_cos_ICOMLBArguments_SetMachineName","comsvcs/ICOMLBArguments::SetMachineName","cos.icomlbarguments_setmachinename"]
old-location: cos\icomlbarguments_setmachinename.htm
tech.root: cos
ms.assetid: 55f9d45e-5c36-4f02-9a9d-111ad4abf016
ms.date: 12/05/2018
ms.keywords: ICOMLBArguments interface [COM+],SetMachineName method, ICOMLBArguments.SetMachineName, ICOMLBArguments::SetMachineName, SetMachineName, SetMachineName method [COM+], SetMachineName method [COM+],ICOMLBArguments interface, _cos_ICOMLBArguments_SetMachineName, comsvcs/ICOMLBArguments::SetMachineName, cos.icomlbarguments_setmachinename
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
 - ICOMLBArguments::SetMachineName
 - comsvcs/ICOMLBArguments::SetMachineName
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
 - ICOMLBArguments.SetMachineName
---

# ICOMLBArguments::SetMachineName


## -description

Sets the computer name for the load balancing server.

## -parameters

### -param cchSvr [in]

The object's machine name.

### -param szServerName [in]

The object's server name.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icomlbarguments">ICOMLBArguments</a>