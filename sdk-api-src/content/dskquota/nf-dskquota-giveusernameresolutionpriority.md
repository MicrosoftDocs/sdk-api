---
UID: NF:dskquota.GiveUserNameResolutionPriority
title: GiveUserNameResolutionPriority function
author: windows-driver-content
description: Places the specified user object next in line for name resolution.
old-location: shell\DiskQuotaControl_GiveUserNameResolutionPriority.htm
old-project: shell
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: DiskQuotaControl object [Windows Shell], GiveUserNameResolutionPriority method, GiveUserNameResolutionPriority, GiveUserNameResolutionPriority method [Windows Shell], GiveUserNameResolutionPriority method [Windows Shell], DiskQuotaControl object, _win32_DiskQuotaControl_GiveUserNameResolutionPriority, shell.DiskQuotaControl_GiveUserNameResolutionPriority
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
-	DiskQuotaControl.GiveUserNameResolutionPriority
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# GiveUserNameResolutionPriority function


## -description


Places the specified user object next in line for name resolution.


## -parameters




### -param pUser

TBD




#### - oUser

Type: <b>Object</b>

An object expression that evaluates to the user's <a href="https://msdn.microsoft.com/0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf">DIDiskQuotaUser</a> object.


## -returns



This method does not return a value.




## -remarks



If asynchronous name resolution is enabled, user objects are placed in a queue.
			By default, they are serviced in the order they are placed in the queue.
			The <b>GiveUserNameResolutionPriority</b> method moves an object to the front of the queue so that it is next in line to be serviced.

Use the <a href="https://msdn.microsoft.com/dc936421-e66d-4762-912a-c586f9cdace4">UserNameResolution</a> property to enable asynchronous name resolution.




## -see-also




<a href="https://msdn.microsoft.com/846297f2-b826-45de-8617-228790e87a63">DiskQuotaControl Object</a>
 

 

