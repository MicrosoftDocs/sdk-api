---
UID: NF:dskquota.ShutdownNameResolution
title: ShutdownNameResolution function
author: windows-driver-content
description: Shuts down the user name resolution thread.
old-location: shell\DiskQuotaControl_ShutdownNameResolution.htm
old-project: shell
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: DiskQuotaControl object [Windows Shell], ShutdownNameResolution method, ShutdownNameResolution, ShutdownNameResolution method [Windows Shell], ShutdownNameResolution method [Windows Shell], DiskQuotaControl object, _win32_DiskQuotaControl_ShutdownNameResolution, shell.DiskQuotaControl_ShutdownNameResolution
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dskquota.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	DiskQuotaControl.ShutdownNameResolution
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# ShutdownNameResolution function


## -description


Shuts down the user name resolution thread.


## -parameters






## -returns



This method does not return a value.




## -remarks



The security identifier (SID) name resolver translates SID to user names on a background thread. This thread is shut down automatically when the associated quota control object is destroyed. However, there are some cases when the thread is no longer needed, but the object is not yet ready to be destroyed.
			A typical example is when no further processing is taking place, but clients are still holding references to the object.
			The <b>ShutdownNameResolution</b> method allows you to terminate the resolver thread and free the associated resources without destroying the quota control object.

<div class="alert"><b>Note</b>   When you shut down the resolver thread, asynchronous name resolution immediately stops. If calls are subsequently made to methods such as <a href="https://msdn.microsoft.com/de20d016-83da-42ac-962f-86faf9b25419">AddUser</a> or <a href="https://msdn.microsoft.com/e5767d28-4c0a-49bc-a1d3-ba809411456d">FindUser</a>, the quota object might re-create the resolver thread.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/846297f2-b826-45de-8617-228790e87a63">DiskQuotaControl Object</a>
 

 

