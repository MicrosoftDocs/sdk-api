---
UID: NF:comsvcs.IObjectContextInfo.GetActivityId
title: IObjectContextInfo::GetActivityId method
author: windows-driver-content
description: Retrieves the identifier of the current activity.
old-location: cos\iobjectcontextinfo_getactivityid.htm
old-project: cossdk
ms.assetid: b6420f2e-223c-4a85-9c45-178a478c8424
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetActivityId method [COM+], GetActivityId method [COM+], IObjectContextInfo interface, GetActivityId,IObjectContextInfo.GetActivityId, IObjectContextInfo, IObjectContextInfo interface [COM+], GetActivityId method, IObjectContextInfo::GetActivityId, _cos_IObjectContextInfo_GetActivityId, comsvcs/IObjectContextInfo::GetActivityId, cos.iobjectcontextinfo_getactivityid
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	IObjectContextInfo.GetActivityId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IObjectContextInfo::GetActivityId method


## -description


Retrieves the identifier of the current activity.


## -parameters




### -param pGUID [out]

A GUID that identifies the current activity.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



If the object is not running within a synchronization domain, COM+ returns a GUID_NULL, which consists of all zeros.




## -see-also




<a href="https://msdn.microsoft.com/50ccf75e-2652-4254-a771-af83cc9248b3">COM+ Contexts and Threading Models</a>



<a href="https://msdn.microsoft.com/76dcc6f3-f840-4672-bba9-038c1249a306">IObjectContextInfo</a>
 

 

