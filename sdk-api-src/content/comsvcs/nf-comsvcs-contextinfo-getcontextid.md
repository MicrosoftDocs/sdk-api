---
UID: NF:comsvcs.ContextInfo.GetContextId
title: ContextInfo::GetContextId (comsvcs.h)
description: Retrieves the unique identifier of this object context.
helpviewer_keywords: ["ContextInfo interface [COM+]","GetContextId method","ContextInfo.GetContextId","ContextInfo::GetContextId","GetContextId","GetContextId method [COM+]","GetContextId method [COM+]","ContextInfo interface","_cos_ContextInfo_GetContextId","comsvcs/ContextInfo::GetContextId","cos.contextinfo_getcontextid"]
old-location: cos\contextinfo_getcontextid.htm
tech.root: cos
ms.assetid: 92566450-8351-49e7-94e1-35a331195322
ms.date: 12/05/2018
ms.keywords: ContextInfo interface [COM+],GetContextId method, ContextInfo.GetContextId, ContextInfo::GetContextId, GetContextId, GetContextId method [COM+], GetContextId method [COM+],ContextInfo interface, _cos_ContextInfo_GetContextId, comsvcs/ContextInfo::GetContextId, cos.contextinfo_getcontextid
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
 - ContextInfo::GetContextId
 - comsvcs/ContextInfo::GetContextId
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
 - ContextInfo.GetContextId
---

# ContextInfo::GetContextId


## -description

Retrieves the unique identifier of this object context.

## -parameters

### -param pbstrCtxId [out]

A reference to the unique identifier.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo">ContextInfo</a>