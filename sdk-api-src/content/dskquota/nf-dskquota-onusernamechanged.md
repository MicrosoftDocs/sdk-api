---
UID: NF:dskquota.OnUserNameChanged
title: OnUserNameChanged function
author: windows-driver-content
description: Occurs when the name information for a DIDiskQuotaUser object has been resolved.
old-location: shell\DiskQuotaControl_OnUserNameChanged.htm
old-project: shell
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: OnUserNameChanged, OnUserNameChanged function [Windows Shell], _win32_DiskQuotaControl_OnUserNameChanged, dskquota/OnUserNameChanged, shell.DiskQuotaControl_OnUserNameChanged
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
-	DllExport
api_location:
-	Shell32.dll
api_name:
-	OnUserNameChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# OnUserNameChanged function


## -description


Occurs when the name information for a <a href="https://msdn.microsoft.com/0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf">DIDiskQuotaUser</a> object has been resolved.


## -parameters




### -param pUser

TBD




#### - oUser

The <b>Object</b> that evaluates to the <a href="https://msdn.microsoft.com/0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf">DIDiskQuotaUser</a> object associated with the user whose name has been resolved.


## -returns



This function does not return a value.




## -remarks



When a client <a href="https://msdn.microsoft.com/0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf">enumerates users</a>, or calls the <a href="https://msdn.microsoft.com/de20d016-83da-42ac-962f-86faf9b25419">AddUser</a> or <a href="https://msdn.microsoft.com/e5767d28-4c0a-49bc-a1d3-ba809411456d">FindUser</a> method, the user name must be resolved to the associated security ID (SID). Because this procedure can be time-consuming, a client can have name resolution done asynchronously on a background thread. When a user's name is resolved, the <a href="https://msdn.microsoft.com/846297f2-b826-45de-8617-228790e87a63">DiskQuotaControl</a> object notifies its client by firing the 
				<b>OnUserNameChanged</b> event. A <b>DIDiskQuotaUser</b> object associated with the user is passed as a parameter. This object allows the client to modify the user's quota settings.




## -see-also




<a href="https://msdn.microsoft.com/846297f2-b826-45de-8617-228790e87a63">DiskQuotaControl Object</a>
 

 

