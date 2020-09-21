---
UID: NF:comsvcs.ContextInfo2.GetApplicationId
title: ContextInfo2::GetApplicationId (comsvcs.h)
description: Retrieves the GUID of the application of the current object context.
helpviewer_keywords: ["ContextInfo2 interface [COM+]","GetApplicationId method","ContextInfo2.GetApplicationId","ContextInfo2::GetApplicationId","GetApplicationId","GetApplicationId method [COM+]","GetApplicationId method [COM+]","ContextInfo2 interface","_cos_ContextInfo2_GetApplicationId","comsvcs/ContextInfo2::GetApplicationId","cos.contextinfo2_getapplicationid"]
old-location: cos\contextinfo2_getapplicationid.htm
tech.root: cos
ms.assetid: 9fc5cffe-a532-4084-8b6c-9812a5b117b2
ms.date: 12/05/2018
ms.keywords: ContextInfo2 interface [COM+],GetApplicationId method, ContextInfo2.GetApplicationId, ContextInfo2::GetApplicationId, GetApplicationId, GetApplicationId method [COM+], GetApplicationId method [COM+],ContextInfo2 interface, _cos_ContextInfo2_GetApplicationId, comsvcs/ContextInfo2::GetApplicationId, cos.contextinfo2_getapplicationid
req.header: comsvcs.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ContextInfo2::GetApplicationId
 - comsvcs/ContextInfo2::GetApplicationId
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
 - ContextInfo2.GetApplicationId
---

# ContextInfo2::GetApplicationId


## -description

 Retrieves the GUID of the application of the current object context.

## -parameters

### -param __MIDL__ContextInfo20001 [out]

A reference to the application identifier.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo2">ContextInfo2</a>