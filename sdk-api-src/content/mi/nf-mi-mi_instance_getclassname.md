---
UID: NF:mi.MI_Instance_GetClassName
title: MI_Instance_GetClassName function
author: windows-sdk-content
description: Gets the class name of the specified instance.
old-location: wmi_v2\mi_instance_getclassname.htm
old-project: wmi_v2
ms.assetid: d2129902-3a2d-479d-b83a-3582094b2fce
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_Instance_GetClassName, MI_Instance_GetClassName function [Windows Management Infrastructure (MI)], mi/MI_Instance_GetClassName, wmi_v2.mi_instance_getclassname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mi.h
req.include-header: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
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
 - MI_Instance_GetClassName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Instance_GetClassName function


## -description


Gets the class name of the specified instance.


## -parameters




### -param self [in]

Instance whose class name will be returned.


### -param className

A pointer to a null-terminated string containing the returned class name.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>
 

 

