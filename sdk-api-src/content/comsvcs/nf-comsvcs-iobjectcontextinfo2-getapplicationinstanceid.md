---
UID: NF:comsvcs.IObjectContextInfo2.GetApplicationInstanceId
title: IObjectContextInfo2::GetApplicationInstanceId
author: windows-driver-content
description: Retrieves the identifier of the application instance of the current object context.
old-location: cos\iobjectcontextinfo2_getapplicationinstanceid.htm
old-project: cossdk
ms.assetid: e20e02c8-23ad-4234-9f20-4e8cae2e9279
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetApplicationInstanceId, GetApplicationInstanceId method [COM+], GetApplicationInstanceId method [COM+],IObjectContextInfo2 interface, IObjectContextInfo2 interface [COM+],GetApplicationInstanceId method, IObjectContextInfo2.GetApplicationInstanceId, IObjectContextInfo2::GetApplicationInstanceId, _cos_IObjectContextInfo2_GetApplicationInstanceId, comsvcs/IObjectContextInfo2::GetApplicationInstanceId, cos.iobjectcontextinfo2_getapplicationinstanceid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IObjectContextInfo2.GetApplicationInstanceId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IObjectContextInfo2::GetApplicationInstanceId


## -description


Retrieves the identifier of the application instance of the current object context. This information is useful when using <a href="https://msdn.microsoft.com/b0ae1b52-b0c5-4f1c-94c6-628d39ef40e3">COM+ Application Recycling</a>, for example.



## -parameters




### -param pGuid [out]

A GUID that identifies the application instance.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/21e078d2-ba93-4118-b1d1-3b4b6e0e28a4">IObjectContextInfo2</a>
 

 

