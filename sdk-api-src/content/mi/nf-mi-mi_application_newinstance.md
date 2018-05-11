---
UID: NF:mi.MI_Application_NewInstance
title: MI_Application_NewInstance function
author: windows-driver-content
description: Creates a new MI_Instance object to be passed to various MI operation APIs that require instances.
old-location: wmi_v2\mi_application_newinstance.htm
old-project: wmi_v2
ms.assetid: e46adc55-c5dc-4395-b746-2ff13cc1e4bb
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: MI_Application_NewInstance, MI_Application_NewInstance function [Windows Management Infrastructure (MI)], mi/MI_Application_NewInstance, wmi_v2.mi_application_newinstance
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
req.typenames: MI_Type
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_Application_NewInstance
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Application_NewInstance function


## -description


Creates a new <a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a> object to be passed to various MI operation APIs that require instances.


## -parameters




### -param application [in]

A pointer to a handle returned from a call to the <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a> function.


### -param className

The class name for the instance being created.


### -param classRTTI [in, optional]

A pointer to optional run time type information for the object being created.


### -param instance

A pointer to the instance returned from this function call.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



When you have finished using the instance created by this call, delete it by calling the <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> function.



