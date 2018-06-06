---
UID: NF:mi.MI_Instance_IsA
title: MI_Instance_IsA function
author: windows-sdk-content
description: Determines if the instance self is an instance of the class given by classDecl.
old-location: wmi_v2\mi_instance_isa.htm
old-project: wmi_v2
ms.assetid: 53fe80b3-cd34-4dee-a474-ced784d61682
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_Instance_IsA, MI_Instance_IsA function [Windows Management Infrastructure (MI)], mi/MI_Instance_IsA, wmi_v2.mi_instance_isa
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
 - MI_Instance_IsA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Instance_IsA function


## -description


Determines if the instance <i>self</i> is an instance of the class given by <i>classDecl</i>.


## -parameters




### -param self [in]

Instance to compare.


### -param classDecl [in]

Class declaration to compare.


### -param flag [out]

Returned value that is set to <b>MI_TRUE</b> if <i>self</i> is an instance of <i>classDecl</i> or if the actual class of the instance inherits from the specified class.  Otherwise, it is set to <b>MI_FALSE</b>.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.



