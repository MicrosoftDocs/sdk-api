---
UID: NF:comsvcs.ObjectContext.get_ContextInfo
title: ObjectContext::get_ContextInfo (comsvcs.h)
description: Retrieves the context information object of the current object's context.
helpviewer_keywords: ["ObjectContext interface [COM+]","get_ContextInfo method","ObjectContext.get_ContextInfo","ObjectContext::get_ContextInfo","_cos_ObjectContext_get_ContextInfo","comsvcs/ObjectContext::get_ContextInfo","cos.objectcontext_get_contextinfo","get_ContextInfo","get_ContextInfo method [COM+]","get_ContextInfo method [COM+]","ObjectContext interface"]
old-location: cos\objectcontext_get_contextinfo.htm
tech.root: cos
ms.assetid: 1974edd5-3348-4ac4-a80c-c549f2d79161
ms.date: 12/05/2018
ms.keywords: ObjectContext interface [COM+],get_ContextInfo method, ObjectContext.get_ContextInfo, ObjectContext::get_ContextInfo, _cos_ObjectContext_get_ContextInfo, comsvcs/ObjectContext::get_ContextInfo, cos.objectcontext_get_contextinfo, get_ContextInfo, get_ContextInfo method [COM+], get_ContextInfo method [COM+],ObjectContext interface
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
 - ObjectContext::get_ContextInfo
 - comsvcs/ObjectContext::get_ContextInfo
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
 - ObjectContext.get_ContextInfo
---

# ObjectContext::get_ContextInfo


## -description

Retrieves the context information object of the current object's context.

## -parameters

### -param ppContextInfo [out]

A reference to a <a href="/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo">ContextInfo</a> interface that contains the context information.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>