---
UID: NF:mi.MI_Application_NewParameterSet
title: MI_Application_NewParameterSet function
author: windows-sdk-content
description: Creates a new parameter set.
old-location: wmi_v2\mi_application_newparameterset.htm
tech.root: WMI_v2
ms.assetid: 9704ad73-78af-4d75-8da6-f327193ea0fa
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: MI_Application_NewParameterSet, MI_Application_NewParameterSet function [Windows Management Infrastructure (MI)], mi/MI_Application_NewParameterSet, wmi_v2.mi_application_newparameterset
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
 - MI_Application_NewParameterSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Application_NewParameterSet function


## -description


Creates a new parameter set.


## -parameters




### -param application [in]

A pointer to a handle returned from the <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a> function.


### -param classRTTI [in, optional]

A pointer to optional run-time type information (RTTI) that defines the property set.  Generally, this is <b>NULL</b> for parameter sets.  If there is no RTTI, call the <a href="https://msdn.microsoft.com/51a26894-f391-4281-9e06-2e70fb662aa2">MI_Instance_AddElement</a> function to add extra parameters. If RTTI is passed in, use the <a href="https://msdn.microsoft.com/581f8d9f-5421-44ab-a3e2-dfb536a35c2c">MI_Instance_SetElement</a> function to set the values of the parameters.


### -param instance

A pointer to a pointer to the instance returned from this function call.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



When you have finished using the parameter set, free the instance by calling the <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> function.



