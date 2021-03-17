---
UID: NF:mi.MI_Instance_GetServerName
title: MI_Instance_GetServerName function (mi.h)
description: Gets the server name from the specified instance.
helpviewer_keywords: ["MI_Instance_GetServerName","MI_Instance_GetServerName function [Windows Management Infrastructure (MI)]","mi/MI_Instance_GetServerName","wmi_v2.mi_instance_getservername"]
old-location: wmi_v2\mi_instance_getservername.htm
tech.root: wmi_v2
ms.assetid: 773b2cb9-9296-4da9-8c13-288524bfccd5
ms.date: 12/05/2018
ms.keywords: MI_Instance_GetServerName, MI_Instance_GetServerName function [Windows Management Infrastructure (MI)], mi/MI_Instance_GetServerName, wmi_v2.mi_instance_getservername
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
 - MI_Instance_GetServerName
 - mi/MI_Instance_GetServerName
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
 - MI_Instance_GetServerName
---

# MI_Instance_GetServerName function


## -description

Gets the server name from the specified instance.

## -parameters

### -param self [in]

Instance whose server name will be returned.

### -param name

Returned server name.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.