---
UID: NF:ktmw32.RecoverEnlistment
title: RecoverEnlistment function
author: windows-sdk-content
description: Recovers an enlistment's state.
old-location: fs\recoverenlistment.htm
tech.root: Ktm
ms.assetid: 5c36732f-bf4f-4071-959e-3359be0b2363
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: RecoverEnlistment, RecoverEnlistment function [Files], fs.recoverenlistment, ktmw32/RecoverEnlistment
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - RecoverEnlistment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RecoverEnlistment
: 
---

# RecoverEnlistment function


## -description


Recovers an enlistment's state.


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment.


### -param EnlistmentKey [in, optional]

The key to the enlistment to be recovered.


## -returns



If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

 The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

