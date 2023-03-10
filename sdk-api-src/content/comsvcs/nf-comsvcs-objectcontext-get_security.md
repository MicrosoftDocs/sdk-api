---
UID: NF:comsvcs.ObjectContext.get_Security
title: ObjectContext::get_Security (comsvcs.h)
description: Retrieves the security object of the current object's context.
helpviewer_keywords: ["ObjectContext interface [COM+]","get_Security method","ObjectContext.get_Security","ObjectContext::get_Security","_cos_ObjectContext_get_Security","comsvcs/ObjectContext::get_Security","cos.objectcontext_get_security","get_Security","get_Security method [COM+]","get_Security method [COM+]","ObjectContext interface"]
old-location: cos\objectcontext_get_security.htm
tech.root: cos
ms.assetid: a160d214-b807-47cd-a712-b4cad941a157
ms.date: 12/05/2018
ms.keywords: ObjectContext interface [COM+],get_Security method, ObjectContext.get_Security, ObjectContext::get_Security, _cos_ObjectContext_get_Security, comsvcs/ObjectContext::get_Security, cos.objectcontext_get_security, get_Security, get_Security method [COM+], get_Security method [COM+],ObjectContext interface
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
 - ObjectContext::get_Security
 - comsvcs/ObjectContext::get_Security
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
 - ObjectContext.get_Security
---

# ObjectContext::get_Security


## -description

Retrieves the security object of the current object's context.

## -parameters

### -param ppSecurityProperty [out]

A reference to a <a href="/windows/desktop/api/comsvcs/nn-comsvcs-securityproperty">SecurityProperty</a> interface that contains the security property of the current object's context.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-objectcontext">ObjectContext</a>