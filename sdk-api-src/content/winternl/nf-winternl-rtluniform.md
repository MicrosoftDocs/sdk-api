---
UID: NF:winternl.RtlUniform
title: RtlUniform function
author: windows-sdk-content
description: Generates a uniform random number using D.H. Lehmer's 1948 algorithm.
old-location: winprog\rtluniform.htm
old-project: DevNotes
ms.assetid: 78bb05fa-3ebc-4e61-ae4f-58544da51200
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: RtlUniform, RtlUniform function [Windows API], winprog.rtluniform, winternl/RtlUniform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: SYNC_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntdll.dll
api_name:
-	RtlUniform
product: Windows
targetos: Windows
req.lib: 
req.dll: Ntdll.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# RtlUniform function


## -description


Generates a uniform random number using D.H. Lehmer's 1948 algorithm.


## -parameters




### -param Seed [in, out]

The seed value.


## -returns



 The function returns a random number uniformly distributed over [0..MAXLONG].




## -remarks



This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Ntdll.dll.




## -see-also




<a href="https://msdn.microsoft.com/3e5a437f-7439-43c9-a191-2908d2df0eb6">CryptGenRandom</a>
 

 

