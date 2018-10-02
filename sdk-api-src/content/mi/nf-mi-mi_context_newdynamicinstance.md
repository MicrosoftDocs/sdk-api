---
UID: NF:mi.MI_Context_NewDynamicInstance
title: MI_Context_NewDynamicInstance function
author: windows-sdk-content
description: Creates a new dynamic instance (weakly typed instance without a class declaration) of a class.
old-location: wmi_v2\mi_context_newdynamicinstance.htm
tech.root: WMI_v2
ms.assetid: 05415945-c804-4056-b4bf-673995c1d6e4
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_Context_NewDynamicInstance, MI_Context_NewDynamicInstance function [Windows Management Infrastructure (MI)], mi/MI_Context_NewDynamicInstance, wmi.mi_newdynamicinstance, wmi_v2.mi_context_newdynamicinstance
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
 - MI_Context_NewDynamicInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Context_NewDynamicInstance function


## -description


Creates a new dynamic instance (weakly typed instance without a class declaration) of a class.


## -parameters




### -param context [in]

A pointer to the request context.


### -param className [in]

The name of the new class.


### -param flags

The create flags (include class meta type).


### -param instance

A pointer to a new instance upon successful return.


## -returns



This function returns MI_INLINE MI_Result MI_INLINE_CALL.




## -remarks



To add elements, call the <a href="https://msdn.microsoft.com/51a26894-f391-4281-9e06-2e70fb662aa2">MI_Instance_AddElement</a> function. When you have finished using the instance, delete it with the <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> function.




## -see-also




<a href="https://msdn.microsoft.com/51a26894-f391-4281-9e06-2e70fb662aa2">MI_Instance_AddElement</a>



<a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a>
 

 

