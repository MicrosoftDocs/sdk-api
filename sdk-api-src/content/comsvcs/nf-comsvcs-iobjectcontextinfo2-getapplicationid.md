---
UID: NF:comsvcs.IObjectContextInfo2.GetApplicationId
title: IObjectContextInfo2::GetApplicationId (comsvcs.h)
description: Retrieves the identifier of the application of the current object context.
helpviewer_keywords: ["GetApplicationId","GetApplicationId method [COM+]","GetApplicationId method [COM+]","IObjectContextInfo2 interface","IObjectContextInfo2 interface [COM+]","GetApplicationId method","IObjectContextInfo2.GetApplicationId","IObjectContextInfo2::GetApplicationId","_cos_IObjectContextInfo2_GetApplicationId","comsvcs/IObjectContextInfo2::GetApplicationId","cos.iobjectcontextinfo2_getapplicationid"]
old-location: cos\iobjectcontextinfo2_getapplicationid.htm
tech.root: cos
ms.assetid: 45cf882a-7a46-4106-a03d-c87c0b52477e
ms.date: 12/05/2018
ms.keywords: GetApplicationId, GetApplicationId method [COM+], GetApplicationId method [COM+],IObjectContextInfo2 interface, IObjectContextInfo2 interface [COM+],GetApplicationId method, IObjectContextInfo2.GetApplicationId, IObjectContextInfo2::GetApplicationId, _cos_IObjectContextInfo2_GetApplicationId, comsvcs/IObjectContextInfo2::GetApplicationId, cos.iobjectcontextinfo2_getapplicationid
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
 - IObjectContextInfo2::GetApplicationId
 - comsvcs/IObjectContextInfo2::GetApplicationId
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
 - IObjectContextInfo2.GetApplicationId
---

# IObjectContextInfo2::GetApplicationId


## -description

Retrieves the identifier of the application of the current object context.

## -parameters

### -param pGuid [out]

A GUID that identifies the application.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo2">IObjectContextInfo2</a>