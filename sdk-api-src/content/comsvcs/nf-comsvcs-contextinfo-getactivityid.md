---
UID: NF:comsvcs.ContextInfo.GetActivityId
title: ContextInfo::GetActivityId (comsvcs.h)
description: Retrieves the activity identifier associated with the object context.
helpviewer_keywords: ["ContextInfo interface [COM+]","GetActivityId method","ContextInfo.GetActivityId","ContextInfo::GetActivityId","GetActivityId","GetActivityId method [COM+]","GetActivityId method [COM+]","ContextInfo interface","_cos_ContextInfo_GetActivityId","comsvcs/ContextInfo::GetActivityId","cos.contextinfo_getactivityid"]
old-location: cos\contextinfo_getactivityid.htm
tech.root: cos
ms.assetid: 1bc87f84-fc98-4ea3-b137-2a88a25d290d
ms.date: 12/05/2018
ms.keywords: ContextInfo interface [COM+],GetActivityId method, ContextInfo.GetActivityId, ContextInfo::GetActivityId, GetActivityId, GetActivityId method [COM+], GetActivityId method [COM+],ContextInfo interface, _cos_ContextInfo_GetActivityId, comsvcs/ContextInfo::GetActivityId, cos.contextinfo_getactivityid
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
 - ContextInfo::GetActivityId
 - comsvcs/ContextInfo::GetActivityId
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
 - ContextInfo.GetActivityId
---

# ContextInfo::GetActivityId


## -description

Retrieves the activity identifier associated with the object context.

## -parameters

### -param pbstrActivityId [out]

A reference to the activity identifier.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-contextinfo">ContextInfo</a>