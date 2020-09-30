---
UID: NF:comsvcs.IObjectContextInfo.GetActivityId
title: IObjectContextInfo::GetActivityId (comsvcs.h)
description: Retrieves the identifier of the current activity.
helpviewer_keywords: ["GetActivityId","GetActivityId method [COM+]","GetActivityId method [COM+]","IObjectContextInfo interface","IObjectContextInfo interface [COM+]","GetActivityId method","IObjectContextInfo.GetActivityId","IObjectContextInfo::GetActivityId","_cos_IObjectContextInfo_GetActivityId","comsvcs/IObjectContextInfo::GetActivityId","cos.iobjectcontextinfo_getactivityid"]
old-location: cos\iobjectcontextinfo_getactivityid.htm
tech.root: cos
ms.assetid: b6420f2e-223c-4a85-9c45-178a478c8424
ms.date: 12/05/2018
ms.keywords: GetActivityId, GetActivityId method [COM+], GetActivityId method [COM+],IObjectContextInfo interface, IObjectContextInfo interface [COM+],GetActivityId method, IObjectContextInfo.GetActivityId, IObjectContextInfo::GetActivityId, _cos_IObjectContextInfo_GetActivityId, comsvcs/IObjectContextInfo::GetActivityId, cos.iobjectcontextinfo_getactivityid
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
 - IObjectContextInfo::GetActivityId
 - comsvcs/IObjectContextInfo::GetActivityId
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
 - IObjectContextInfo.GetActivityId
---

# IObjectContextInfo::GetActivityId


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

<a href="/windows/desktop/cossdk/com--contexts-and-threading-models">COM+ Contexts and Threading Models</a>



<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextinfo">IObjectContextInfo</a>