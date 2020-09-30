---
UID: NF:mi.MI_Class_GetServerName
title: MI_Class_GetServerName function (mi.h)
description: Gets the name of the server from the specified class.
helpviewer_keywords: ["MI_Class_GetServerName","MI_Class_GetServerName function [Windows Management Infrastructure (MI)]","mi/MI_Class_GetServerName","wmi_v2.mi_class_getservername"]
old-location: wmi_v2\mi_class_getservername.htm
tech.root: wmi_v2
ms.assetid: bb7312a0-f851-44a4-8467-31bbe1a9ac41
ms.date: 12/05/2018
ms.keywords: MI_Class_GetServerName, MI_Class_GetServerName function [Windows Management Infrastructure (MI)], mi/MI_Class_GetServerName, wmi_v2.mi_class_getservername
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
 - MI_Class_GetServerName
 - mi/MI_Class_GetServerName
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
 - MI_Class_GetServerName
---

# MI_Class_GetServerName function


## -description

Gets the name of the server from the specified class.

## -parameters

### -param self [in]

A pointer to the class from which to retrieve the server name.

### -param serverName

A pointer to a pointer to the returned server name. This string is owned by the class and does not need to be deleted.

## -returns

This function returns MI_INLINE MI_Result.

