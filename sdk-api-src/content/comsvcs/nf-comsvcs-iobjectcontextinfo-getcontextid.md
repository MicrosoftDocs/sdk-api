---
UID: NF:comsvcs.IObjectContextInfo.GetContextId
title: IObjectContextInfo::GetContextId (comsvcs.h)
description: Retrieves the identifier of the current context.
helpviewer_keywords: ["GetContextId","GetContextId method [COM+]","GetContextId method [COM+]","IObjectContextInfo interface","IObjectContextInfo interface [COM+]","GetContextId method","IObjectContextInfo.GetContextId","IObjectContextInfo::GetContextId","_cos_IObjectContextInfo_GetContextId","comsvcs/IObjectContextInfo::GetContextId","cos.iobjectcontextinfo_getcontextid"]
old-location: cos\iobjectcontextinfo_getcontextid.htm
tech.root: cos
ms.assetid: 97059f07-161f-451f-9f9b-b4dd81b7bf79
ms.date: 12/05/2018
ms.keywords: GetContextId, GetContextId method [COM+], GetContextId method [COM+],IObjectContextInfo interface, IObjectContextInfo interface [COM+],GetContextId method, IObjectContextInfo.GetContextId, IObjectContextInfo::GetContextId, _cos_IObjectContextInfo_GetContextId, comsvcs/IObjectContextInfo::GetContextId, cos.iobjectcontextinfo_getcontextid
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
 - IObjectContextInfo::GetContextId
 - comsvcs/IObjectContextInfo::GetContextId
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
 - IObjectContextInfo.GetContextId
---

# IObjectContextInfo::GetContextId


## -description

Retrieves the identifier of the current context.

## -parameters

### -param pGuid [out]

A GUID that identifies the current context.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo">IObjectContextInfo</a>