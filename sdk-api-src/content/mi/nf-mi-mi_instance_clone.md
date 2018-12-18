---
UID: NF:mi.MI_Instance_Clone
title: MI_Instance_Clone function
author: windows-sdk-content
description: Creates a copy of the specified instance on the heap.
old-location: wmi_v2\mi_instance_clone.htm
tech.root: wmi_v2
ms.assetid: 9c7a4659-5bc4-4d24-89bc-9da4f2bdf107
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MI_Instance_Clone, MI_Instance_Clone function [Windows Management Infrastructure (MI)], mi/MI_Instance_Clone, wmi_v2.mi_instance_clone
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
 - MI_Instance_Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Instance_Clone function


## -description


Creates a copy of the specified instance on the heap.


## -parameters




### -param self [in]

Instance to be cloned.


### -param newInstance

Returned instance. This should be deleted via <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a>.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



