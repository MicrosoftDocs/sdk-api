---
UID: NF:mi.MI_Operation_GetSession
title: MI_Operation_GetSession function (mi.h)
description: Gets the session associated with an operation.
helpviewer_keywords: ["MI_Operation_GetSession","MI_Operation_GetSession function [Windows Management Infrastructure (MI)]","mi/MI_Operation_GetSession","wmi_v2.mi_operation_getsession"]
old-location: wmi_v2\mi_operation_getsession.htm
tech.root: wmi_v2
ms.assetid: 710ccbc5-956c-4bb3-b93b-f61a449c08ef
ms.date: 12/05/2018
ms.keywords: MI_Operation_GetSession, MI_Operation_GetSession function [Windows Management Infrastructure (MI)], mi/MI_Operation_GetSession, wmi_v2.mi_operation_getsession
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Operation_GetSession
 - mi/MI_Operation_GetSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Operation_GetSession
---

# MI_Operation_GetSession function


## -description

Gets the session associated with an operation.

## -parameters

### -param operation [in]

Operation handle returned from an instance session operation.

### -param session [out]

Returned session that was used to create the operation. Copy of the parent session that initiated the operation.

## -remarks

This function is useful in a result asynchronous callback if a new operation needs to be initiated against the same session.

