---
UID: NF:mi.MI_ParameterSet_GetParameterAt
title: MI_ParameterSet_GetParameterAt function
author: windows-sdk-content
description: Gets a method's parameter information at the specified index.
old-location: wmi_v2\mi_parameterset_getparameterat.htm
old-project: wmi_v2
ms.assetid: fcfd7104-dd63-4a48-9a20-dcec0dc33242
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: MI_ParameterSet_GetParameterAt, MI_ParameterSet_GetParameterAt function [Windows Management Infrastructure (MI)], mi/MI_ParameterSet_GetParameterAt, wmi_v2.mi_parameterset_getparameterat
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_ParameterSet_GetParameterAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_ParameterSet_GetParameterAt function


## -description


Gets a method's parameter information at the specified index.


## -parameters




### -param self [in]


<a href="https://msdn.microsoft.com/14b5773c-4741-453b-824a-226aab9b8a10">MI_ParameterSet</a> structure.


### -param index

Zero-based index of the parameter.


### -param name

Returned parameter name.


### -param parameterType [out]

Returned parameter type.


### -param referenceClass

Returned reference class.


### -param qualifierSet [out]

Returned qualifier set of the parameter.


## -returns



This function returns MI_INLINE MI_Result.



