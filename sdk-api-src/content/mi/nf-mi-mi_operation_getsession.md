---
UID: NF:mi.MI_Operation_GetSession
title: MI_Operation_GetSession function
author: windows-sdk-content
description: Gets the session associated with an operation.
old-location: wmi_v2\mi_operation_getsession.htm
old-project: wmi_v2
ms.assetid: 710ccbc5-956c-4bb3-b93b-f61a449c08ef
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: MI_Operation_GetSession, MI_Operation_GetSession function [Windows Management Infrastructure (MI)], mi/MI_Operation_GetSession, wmi_v2.mi_operation_getsession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Operation_GetSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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



