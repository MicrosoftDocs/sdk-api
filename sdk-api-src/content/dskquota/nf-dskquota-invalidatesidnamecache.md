---
UID: NF:dskquota.InvalidateSidNameCache
title: InvalidateSidNameCache function
author: windows-driver-content
description: Invalidates the security ID user name cache.
old-location: shell\DiskQuotaControl_InvalidateSidNameCache.htm
old-project: shell
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: DiskQuotaControl object [Windows Shell], InvalidateSidNameCache method, InvalidateSidNameCache, InvalidateSidNameCache method [Windows Shell], InvalidateSidNameCache method [Windows Shell], DiskQuotaControl object, _win32_DiskQuotaControl_InvalidateSidNameCache, shell.DiskQuotaControl_InvalidateSidNameCache
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
-	DiskQuotaControl.InvalidateSidNameCache
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# InvalidateSidNameCache function


## -description


Invalidates the security ID user name cache.


## -parameters






## -returns



This method does not return a value.




## -remarks



User names and associated security IDs are stored in a cache. You can clear this cache by calling <b>InvalidateSidNameCache</b>.
			If you subsequently create a new user object, the information will have to be obtained from the domain controller, and the cache will have to be reestablished.




## -see-also




<a href="https://msdn.microsoft.com/846297f2-b826-45de-8617-228790e87a63">DiskQuotaControl Object</a>
 

 

