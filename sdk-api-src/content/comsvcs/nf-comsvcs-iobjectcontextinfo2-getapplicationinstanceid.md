---
UID: NF:comsvcs.IObjectContextInfo2.GetApplicationInstanceId
title: IObjectContextInfo2::GetApplicationInstanceId (comsvcs.h)
description: Retrieves the identifier of the application instance of the current object context.
helpviewer_keywords: ["GetApplicationInstanceId","GetApplicationInstanceId method [COM+]","GetApplicationInstanceId method [COM+]","IObjectContextInfo2 interface","IObjectContextInfo2 interface [COM+]","GetApplicationInstanceId method","IObjectContextInfo2.GetApplicationInstanceId","IObjectContextInfo2::GetApplicationInstanceId","_cos_IObjectContextInfo2_GetApplicationInstanceId","comsvcs/IObjectContextInfo2::GetApplicationInstanceId","cos.iobjectcontextinfo2_getapplicationinstanceid"]
old-location: cos\iobjectcontextinfo2_getapplicationinstanceid.htm
tech.root: cos
ms.assetid: e20e02c8-23ad-4234-9f20-4e8cae2e9279
ms.date: 12/05/2018
ms.keywords: GetApplicationInstanceId, GetApplicationInstanceId method [COM+], GetApplicationInstanceId method [COM+],IObjectContextInfo2 interface, IObjectContextInfo2 interface [COM+],GetApplicationInstanceId method, IObjectContextInfo2.GetApplicationInstanceId, IObjectContextInfo2::GetApplicationInstanceId, _cos_IObjectContextInfo2_GetApplicationInstanceId, comsvcs/IObjectContextInfo2::GetApplicationInstanceId, cos.iobjectcontextinfo2_getapplicationinstanceid
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
 - IObjectContextInfo2::GetApplicationInstanceId
 - comsvcs/IObjectContextInfo2::GetApplicationInstanceId
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
 - IObjectContextInfo2.GetApplicationInstanceId
---

# IObjectContextInfo2::GetApplicationInstanceId


## -description

Retrieves the identifier of the application instance of the current object context. This information is useful when using <a href="/windows/desktop/cossdk/com--application-recycling">COM+ Application Recycling</a>, for example.

## -parameters

### -param pGuid [out]

A GUID that identifies the application instance.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo2">IObjectContextInfo2</a>