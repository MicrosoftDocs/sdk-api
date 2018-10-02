---
UID: NF:mi.MI_Application_NewOperationOptions
title: MI_Application_NewOperationOptions function
author: windows-sdk-content
description: Creates an MI_OperationOptions object that can be used with the operation functions on the MI_Session object.
old-location: wmi_v2\mi_application_newoperationoptions.htm
tech.root: WMI_v2
ms.assetid: 0b9f569b-bb32-4393-9fd2-9d5d601c2214
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MI_Application_NewOperationOptions, MI_Application_NewOperationOptions function [Windows Management Infrastructure (MI)], mi/MI_Application_NewOperationOptions, wmi_v2.mi_application_newoperationoptions
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
 - MI_Application_NewOperationOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
---

# MI_Application_NewOperationOptions function


## -description


Creates an <a href="https://msdn.microsoft.com/60445a53-c40c-4d0a-9650-21d0c7f3bbf6">MI_OperationOptions</a> object that can be used with the operation functions on the <a href="https://msdn.microsoft.com/68a69321-0aa9-423e-a72f-aa2f4dee2d51">MI_Session</a> object.


## -parameters




### -param application [in]

A pointer to a handle returned from the <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a> function.


### -param mustUnderstand

Specifies if the transport and provider are required to process the options being passed. This should be set to <b>MI_FALSE</b>. Setting this parameter to <b>MI_TRUE</b> can cause the operation to fail if the server cannot process one of the options.


### -param options [out]

A pointer to an options handle returned from this function.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



When you have finished using the object returned from this call, delete it by calling the <a href="https://msdn.microsoft.com/a9e43835-92a4-468a-9d45-1d4ab81d94f0">MI_OperationOptions_Delete</a> function.



