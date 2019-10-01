---
UID: NF:mi.MI_Instance_ClearElement
title: MI_Instance_ClearElement function (mi.h)
author: windows-sdk-content
description: Clears the value of the named element (CIM property) and sets it to NULL.
old-location: wmi_v2\mi_instance_clearelement.htm
tech.root: wmi_v2
ms.assetid: de945902-4b10-47d1-a374-a1aeab02a787
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MI_Instance_ClearElement, MI_Instance_ClearElement function [Windows Management Infrastructure (MI)], mi/MI_Instance_ClearElement, wmi_v2.mi_instance_clearelement
ms.topic: function
f1_keywords:
- mi/MI_Instance_ClearElement
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
- MI_Instance_ClearElement
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_Instance_ClearElement function


## -description


Clears the value of the named element (CIM property) and sets it to <b>NULL</b>.


## -parameters




### -param self [in, out]

Instance whose property will be set.


### -param name

A null-terminated string that represents the name of the property that will be cleared.


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_addelement">MI_Instance_AddElement</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_getelement">MI_Instance_GetElement</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_setelement">MI_Instance_SetElement</a>
 

 

