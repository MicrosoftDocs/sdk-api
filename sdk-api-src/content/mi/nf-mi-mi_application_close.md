---
UID: NF:mi.MI_Application_Close
title: MI_Application_Close function
author: windows-sdk-content
description: Deinitializes the management infrastructure client API that was initialized through a call to MI_Application_Initialize.
old-location: wmi_v2\mi_application_close.htm
old-project: wmi_v2
ms.assetid: e5ad3ed3-8ef6-4bb5-999a-7d2ee91f51d5
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_Application_Close, MI_Application_Close function [Windows Management Infrastructure (MI)], mi/MI_Application_Close, wmi_v2.mi_application_close
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
 - MI_Application_Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Application_Close function


## -description


Deinitializes the management infrastructure client API that was initialized through a call to <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a>.


## -parameters




### -param application [in, out]

Application handle that was initialized through a call to <a href="https://msdn.microsoft.com/32696A33-820D-4D01-AF71-DDA1F34EFBE0">MI_Application_Initialize</a>.


## -returns



This function returns MI_INLINE MI_Result.




## -remarks



<b>MI_Application_Close</b> will unload the entire protocol handling infrastructure and background threads associated with the infrastructure.

<b>MI_Application_Close</b> cancels all active sessions and operations.  Sessions created under the target application and those sessions' operations must close before this function will return. Once the API does so, Mi.dll can be unloaded and any caches held within the MI infrastructure are flushed.

<b>MI_Application_Close</b> must not be called from within an asynchronous callback, otherwise it will cause deadlocks.

To avoid a system hang when calling this function, reference count <a href="https://msdn.microsoft.com/da486ade-88ef-40c4-8151-356e718da7db">MI_Application</a> and call the <b>MI_Application_Close</b> function only when the AppDomain is shutting down and after all sessions have been closed.



