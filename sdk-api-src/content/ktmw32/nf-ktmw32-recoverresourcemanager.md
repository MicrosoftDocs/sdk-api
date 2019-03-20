---
UID: NF:ktmw32.RecoverResourceManager
title: RecoverResourceManager function (ktmw32.h)
author: windows-sdk-content
description: Recovers a resource manager's state from its log file.
old-location: fs\recoverresourcemanager.htm
tech.root: ktm
ms.assetid: 616ff873-c0d0-464e-9b1b-74a426b99abd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RecoverResourceManager, RecoverResourceManager function [Files], fs.recoverresourcemanager, ktmw32/RecoverResourceManager
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
 - RecoverResourceManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RecoverResourceManager function


## -description


Recovers a resource manager's state from its log file.


## -parameters




### -param ResourceManagerHandle [in]

A handle to the resource manager.


## -returns



If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

 The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

