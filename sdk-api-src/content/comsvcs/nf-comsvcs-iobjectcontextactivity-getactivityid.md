---
UID: NF:comsvcs.IObjectContextActivity.GetActivityId
title: IObjectContextActivity::GetActivityId (comsvcs.h)
description: Retrieves the GUID associated with the current activity.
helpviewer_keywords: ["GetActivityId","GetActivityId method [COM+]","GetActivityId method [COM+]","IObjectContextActivity interface","IObjectContextActivity interface [COM+]","GetActivityId method","IObjectContextActivity.GetActivityId","IObjectContextActivity::GetActivityId","_cos_IObjectContextActivity_GetActivityID","comsvcs/IObjectContextActivity::GetActivityId","cos.iobjectcontextactivity_getactivityid"]
old-location: cos\iobjectcontextactivity_getactivityid.htm
tech.root: cos
ms.assetid: 027d92b7-17dc-4ee5-a85a-e00b425a7a7a
ms.date: 12/05/2018
ms.keywords: GetActivityId, GetActivityId method [COM+], GetActivityId method [COM+],IObjectContextActivity interface, IObjectContextActivity interface [COM+],GetActivityId method, IObjectContextActivity.GetActivityId, IObjectContextActivity::GetActivityId, _cos_IObjectContextActivity_GetActivityID, comsvcs/IObjectContextActivity::GetActivityId, cos.iobjectcontextactivity_getactivityid
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
 - IObjectContextActivity::GetActivityId
 - comsvcs/IObjectContextActivity::GetActivityId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - comsvcs.h
api_name:
 - IObjectContextActivity.GetActivityId
---

# IObjectContextActivity::GetActivityId


## -description

Retrieves the GUID associated with the current activity.

## -parameters

### -param pGUID [out]

A reference to the GUID associated with the current activity.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-iobjectcontextactivity">IObjectContextActivity</a>