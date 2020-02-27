---
UID: NF:comsvcs.ContextInfo2.GetApplicationInstanceId
title: ContextInfo2::GetApplicationInstanceId (comsvcs.h)
description: Retrieves the GUID of the application instance of the current object context.
old-location: cos\contextinfo2_getapplicationinstanceid.htm
tech.root: cossdk
ms.assetid: 77149329-db3a-4ff4-a522-c290c2d0a915
ms.date: 12/05/2018
ms.keywords: ContextInfo2 interface [COM+],GetApplicationInstanceId method, ContextInfo2.GetApplicationInstanceId, ContextInfo2::GetApplicationInstanceId, GetApplicationInstanceId, GetApplicationInstanceId method [COM+], GetApplicationInstanceId method [COM+],ContextInfo2 interface, _cos_ContextInfo2_GetApplicationInstanceId, comsvcs/ContextInfo2::GetApplicationInstanceId, cos.contextinfo2_getapplicationinstanceid
f1_keywords:
- comsvcs/ContextInfo2.GetApplicationInstanceId
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComSvcs.h
api_name:
- ContextInfo2.GetApplicationInstanceId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ContextInfo2::GetApplicationInstanceId


## -description


Retrieves the GUID of the application instance of the current object context.

This information is useful when using <a href="https://docs.microsoft.com/windows/desktop/cossdk/com--application-recycling">COM+ Application Recycling</a>, for example.



## -parameters




### -param __MIDL__ContextInfo20002 [out]

A reference to the application instance identifier.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo2">ContextInfo2</a>
 

 

