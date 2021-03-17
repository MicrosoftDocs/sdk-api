---
UID: NF:comsvcs.ISecurityCallContext.get_Count
title: ISecurityCallContext::get_Count (comsvcs.h)
description: Retrieves the number of properties in the security context collection.
helpviewer_keywords: ["ISecurityCallContext interface [COM+]","get_Count method","ISecurityCallContext.get_Count","ISecurityCallContext::get_Count","_cos_ISecurityCallContext_get_Count","comsvcs/ISecurityCallContext::get_Count","cos.isecuritycallcontext_get_count","get_Count","get_Count method [COM+]","get_Count method [COM+]","ISecurityCallContext interface"]
old-location: cos\isecuritycallcontext_get_count.htm
tech.root: cos
ms.assetid: aebb28de-79ee-4cec-afb9-cfb067a4fb62
ms.date: 12/05/2018
ms.keywords: ISecurityCallContext interface [COM+],get_Count method, ISecurityCallContext.get_Count, ISecurityCallContext::get_Count, _cos_ISecurityCallContext_get_Count, comsvcs/ISecurityCallContext::get_Count, cos.isecuritycallcontext_get_count, get_Count, get_Count method [COM+], get_Count method [COM+],ISecurityCallContext interface
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
 - ISecurityCallContext::get_Count
 - comsvcs/ISecurityCallContext::get_Count
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
 - ISecurityCallContext.get_Count
---

# ISecurityCallContext::get_Count


## -description

Retrieves the number of properties in the security context collection.

## -parameters

### -param plCount [out]

The number of named security call context properties.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-isecuritycallcontext">ISecurityCallContext</a>