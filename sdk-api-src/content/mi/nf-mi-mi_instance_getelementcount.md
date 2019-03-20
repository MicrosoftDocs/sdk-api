---
UID: NF:mi.MI_Instance_GetElementCount
title: MI_Instance_GetElementCount function (mi.h)
author: windows-sdk-content
description: Gets the number of elements in an instance.
old-location: wmi_v2\mi_instance_getelementcount.htm
tech.root: wmi_v2
ms.assetid: a378bde1-c164-4905-82f8-f771f8da60ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_Instance_GetElementCount, MI_Instance_GetElementCount function [Windows Management Infrastructure (MI)], mi/MI_Instance_GetElementCount, wmi_v2.mi_instance_getelementcount
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
 - MI_Instance_GetElementCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Instance_GetElementCount function


## -description


Gets the number of elements in an instance.


## -parameters




### -param self [in]

Instance whose element count will be returned.


### -param count [out]

Returned number of elements in the instance.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



