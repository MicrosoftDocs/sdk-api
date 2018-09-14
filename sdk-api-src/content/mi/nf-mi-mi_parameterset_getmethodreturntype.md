---
UID: NF:mi.MI_ParameterSet_GetMethodReturnType
title: MI_ParameterSet_GetMethodReturnType function
author: windows-sdk-content
description: Gets the method return type and qualifier set for a specified parameter set.
old-location: wmi_v2\mi_parameterset_getmethodreturntype.htm
tech.root: WMI_v2
ms.assetid: 8d2e881a-72a8-4819-a407-b7381ab7a94a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: MI_ParameterSet_GetMethodReturnType, MI_ParameterSet_GetMethodReturnType function [Windows Management Infrastructure (MI)], mi/MI_ParameterSet_GetMethodReturnType, wmi_v2.mi_parameterset_getmethodreturntype
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MI_ParameterSet_GetMethodReturnType
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_ParameterSet_GetMethodReturnType function


## -description


Gets the method return type and qualifier set for a specified parameter set.


## -parameters




### -param self [in]


<a href="https://msdn.microsoft.com/14b5773c-4741-453b-824a-226aab9b8a10">MI_ParameterSet</a> structure.


### -param returnType [out]

Returned method return type.


### -param qualifierSet [out]

The returned qualifier set for the method name and return type.


## -returns



This function returns MI_INLINE MI_Result.



