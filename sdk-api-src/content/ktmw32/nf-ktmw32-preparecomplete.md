---
UID: NF:ktmw32.PrepareComplete
title: PrepareComplete function
author: windows-sdk-content
description: Indicates that the resource manager (RM) has completed all processing necessary to guarantee that a commit or abort operation will succeed for the specified transaction.
old-location: fs\preparecomplete.htm
tech.root: ktm
ms.assetid: 47488c70-3409-4544-bcca-3415f91e7194
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PrepareComplete, PrepareComplete function [Files], fs.preparecomplete, ktmw32/PrepareComplete
ms.topic: function
req.header: ktmw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - PrepareComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PrepareComplete function


## -description


Indicates that the resource manager (RM) has completed all processing necessary to guarantee that a commit or abort operation will succeed for the specified transaction.


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment.


### -param TmVirtualClock [in]

The latest virtual clock value received for this prepare complete notification. If you specify <b>NULL</b>, the virtual clock value is not changed. See <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>.

To change the virtual clock value, this value must be greater than the current value returned in the COMMIT notification.


## -returns



If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

 The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/21d7c0fa-3a49-43b3-9325-d3dfdabbcb98">GetCurrentClockTransactionManager</a>



<a href="https://msdn.microsoft.com/d606f960-e843-4478-8ba7-5201f85c44ce">GetNotificationResourceManager</a>



<a href="https://msdn.microsoft.com/c83e104b-6cd7-4399-8232-7c2e7b408f1a">GetNotificationResourceManagerAsync</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/b4a70a51-2c49-4626-9fca-9ca6e0d21a53">PrePrepareComplete</a>
 

 

