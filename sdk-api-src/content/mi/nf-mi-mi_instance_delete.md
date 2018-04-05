---
UID: NF:mi.MI_Instance_Delete
title: MI_Instance_Delete function
author: windows-driver-content
description: Deletes an instance that was created on the heap or cloned from another instance.
old-location: wmi_v2\mi_instance_delete.htm
old-project: wmi_v2
ms.assetid: 6370e464-b262-4c91-a3c8-889911df7965
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: MI_Instance_Delete, MI_Instance_Delete function [Windows Management Infrastructure (MI)], mi/MI_Instance_Delete, wmi_v2.mi_instance_delete
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
-	MI_Instance_Delete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Instance_Delete function


## -description


Deletes an instance that was created on the heap or cloned from another instance.


## -parameters




### -param self [in, out]

Instance to be released.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



Instances created with the <a href="https://msdn.microsoft.com/9c7a4659-5bc4-4d24-89bc-9da4f2bdf107">MI_Instance_Clone</a>, <a href="https://msdn.microsoft.com/e46adc55-c5dc-4395-b746-2ff13cc1e4bb">MI_Application_NewInstance</a>, <a href="https://msdn.microsoft.com/59571aa0-7fc2-4724-94e8-15b8a62327b6">MI_Context_NewInstance</a>, <a href="https://msdn.microsoft.com/05415945-c804-4056-b4bf-673995c1d6e4">MI_Context_NewDynamicInstance</a>, <a href="https://msdn.microsoft.com/8fb80e6f-627c-4897-9776-7454c0258809">MI_Context_NewParameters</a>, and <a href="https://msdn.microsoft.com/dab6226b-5769-4e2f-abd2-b89cc2d9911e">MI_Utilities_CimErrorFromErrorCode</a> functions should be passed to this function when they are no longer required.




## -see-also




<a href="https://msdn.microsoft.com/e46adc55-c5dc-4395-b746-2ff13cc1e4bb">MI_Application_NewInstance</a>



<a href="https://msdn.microsoft.com/05415945-c804-4056-b4bf-673995c1d6e4">MI_Context_NewDynamicInstance</a>



<a href="https://msdn.microsoft.com/59571aa0-7fc2-4724-94e8-15b8a62327b6">MI_Context_NewInstance</a>



<a href="https://msdn.microsoft.com/8fb80e6f-627c-4897-9776-7454c0258809">MI_Context_NewParameters</a>



<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>



<a href="https://msdn.microsoft.com/9c7a4659-5bc4-4d24-89bc-9da4f2bdf107">MI_Instance_Clone</a>



<a href="https://msdn.microsoft.com/dab6226b-5769-4e2f-abd2-b89cc2d9911e">MI_Utilities_CimErrorFromErrorCode</a>
 

 

