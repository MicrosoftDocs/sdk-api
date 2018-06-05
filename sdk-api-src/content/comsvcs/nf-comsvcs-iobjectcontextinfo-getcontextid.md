---
UID: NF:comsvcs.IObjectContextInfo.GetContextId
title: IObjectContextInfo::GetContextId
author: windows-sdk-content
description: Retrieves the identifier of the current context.
old-location: cos\iobjectcontextinfo_getcontextid.htm
old-project: cossdk
ms.assetid: 97059f07-161f-451f-9f9b-b4dd81b7bf79
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetContextId, GetContextId method [COM+], GetContextId method [COM+],IObjectContextInfo interface, IObjectContextInfo interface [COM+],GetContextId method, IObjectContextInfo.GetContextId, IObjectContextInfo::GetContextId, _cos_IObjectContextInfo_GetContextId, comsvcs/IObjectContextInfo::GetContextId, cos.iobjectcontextinfo_getcontextid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IObjectContextInfo.GetContextId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/50ccf75e-2652-4254-a771-af83cc9248b3">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/76dcc6f3-f840-4672-bba9-038c1249a306">IObjectContextInfo</a>
 

 

