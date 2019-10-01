---
UID: NF:mi.MI_Instance_GetNameSpace
title: MI_Instance_GetNameSpace function (mi.h)
author: windows-sdk-content
description: Gets the namespace name of the specified instance.
old-location: wmi_v2\mi_instance_getnamespace.htm
tech.root: wmi_v2
ms.assetid: 885423d6-c247-4d45-a5fd-a1a18bd5e6e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_Instance_GetNameSpace, MI_Instance_GetNameSpace function [Windows Management Infrastructure (MI)], mi/MI_Instance_GetNameSpace, wmi_v2.mi_instance_getnamespace
ms.topic: function
f1_keywords:
- mi/MI_Instance_GetNameSpace
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Mi.h
api_name:
- MI_Instance_GetNameSpace
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_Instance_GetNameSpace function


## -description


Gets the namespace name of the specified instance.


## -parameters




### -param self [in]

Instance whose namespace name is to be returned.


### -param nameSpace

Returned namespace name.


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



