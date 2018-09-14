---
UID: NF:mi.MI_ParameterSet_GetParameter
title: MI_ParameterSet_GetParameter function
author: windows-sdk-content
description: Gets a method's parameter information based on a parameter name.
old-location: wmi_v2\mi_parameterset_getparameter.htm
tech.root: WMI_v2
ms.assetid: ff895beb-8354-488d-9c97-2d0448da954a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: MI_ParameterSet_GetParameter, MI_ParameterSet_GetParameter function [Windows Management Infrastructure (MI)], mi/MI_ParameterSet_GetParameter, wmi_v2.mi_parameterset_getparameter
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
 - MI_ParameterSet_GetParameter
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_ParameterSet_GetParameter function


## -description


Gets a method's parameter information based on a parameter name.


## -parameters




### -param self [in]


<a href="https://msdn.microsoft.com/14b5773c-4741-453b-824a-226aab9b8a10">MI_ParameterSet</a> structure.


### -param name [in]

Name of the parameter to get.


### -param parameterType [out]

Returned parameter type.


### -param referenceClass [out]

Returned reference class.


### -param qualifierSet [out]

Returned qualifier set of the parameter.


### -param index [out]

Returned zero-based index of the parameter.


## -returns



This function returns MI_INLINE MI_Result.



