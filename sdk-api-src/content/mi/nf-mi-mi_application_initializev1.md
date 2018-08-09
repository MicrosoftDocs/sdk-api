---
UID: NF:mi.MI_Application_InitializeV1
title: MI_Application_InitializeV1 function
author: windows-sdk-content
description: Initializes an application so that it can make Management Infrastructure (MI) client API calls.
old-location: wmi_v2\mi_application_initialize.htm
old-project: wmi_v2
ms.assetid: 32696A33-820D-4D01-AF71-DDA1F34EFBE0
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_Application_Initialize, MI_Application_Initialize function [Windows Management Infrastructure (MI)], MI_Application_InitializeV1, MI_Application_InitializeV1 function [Windows Management Infrastructure (MI)], mi/MI_Application_Initialize, mi/MI_Application_InitializeV1, wmi_v2.mi_application_initialize
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
 - DllExport
api_location:
 - Mi.dll
 - Wmidcom.dll
 - WsmSvc.dll
api_name:
 - MI_Application_InitializeV1
 - MI_Application_Initialize
product: Windows
targetos: Windows
req.lib: Mi.lib
req.dll: Mi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MI_Application_InitializeV1 function


## -description


Initializes an application so that it can make Management Infrastructure (MI) client API 
    calls.


## -parameters




### -param flags

Must be 0.


### -param applicationID [in, optional]

An optional string (usually <b>GUID</b> in string format) to represent a client 
    application. This string may be used for application specific configuration and application specific 
  logging.


### -param extendedError [out, optional]

Optional parameter giving more error information if the operation failed. If an instance is returned, 
      <a href="https://msdn.microsoft.com/6370e464-b262-4c91-a3c8-889911df7965">MI_Instance_Delete</a> must  be called to free it 
      when it is no longer needed.


### -param application [out]

A pointer to an uninitialized <a href="https://msdn.microsoft.com/da486ade-88ef-40c4-8151-356e718da7db">MI_Application</a> 
      handle is passed in and a populated handle is returned. The initialized handle must be passed to 
      <a href="https://msdn.microsoft.com/e5ad3ed3-8ef6-4bb5-999a-7d2ee91f51d5">MI_Application_Close</a> before the application 
  shuts down. If an application passes this handle, pass it by value rather than as a pointer.


## -returns



This function returns MI_Result MI_MAIN_CALL.




## -remarks



This API needs to be called only once per application; although, it can be called multiple times safely. 
    Calling this API multiple times will result in a small amount of extra memory usage.  When called, the application 
    passes in an <a href="https://msdn.microsoft.com/da486ade-88ef-40c4-8151-356e718da7db">MI_Application</a> pointer to be initialized. 
    This pointer must be closed by calling 
    <a href="https://msdn.microsoft.com/e5ad3ed3-8ef6-4bb5-999a-7d2ee91f51d5">MI_Application_Close</a>. Not doing so will cause 
    memory leaks and potential crashes during shutdown.

MI.h defines 
     <b>MI_Application_Initialize</b> as 
   <b>MI_Application_InitializeV1</b> with this 
     line:

<code>#define MI_Application_Initialize MI_Application_InitializeV1</code>



