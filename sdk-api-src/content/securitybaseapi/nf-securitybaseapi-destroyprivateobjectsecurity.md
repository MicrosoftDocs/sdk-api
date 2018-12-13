---
UID: NF:securitybaseapi.DestroyPrivateObjectSecurity
title: DestroyPrivateObjectSecurity function
author: windows-sdk-content
description: Deletes a private object's security descriptor.
old-location: security\destroyprivateobjectsecurity.htm
tech.root: secauthz
ms.assetid: 4ef10852-8229-41de-a4d7-d2845e4c92ce
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DestroyPrivateObjectSecurity, DestroyPrivateObjectSecurity function [Security], _win32_destroyprivateobjectsecurity, security.destroyprivateobjectsecurity, securitybaseapi/DestroyPrivateObjectSecurity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - DestroyPrivateObjectSecurity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DestroyPrivateObjectSecurity function


## -description


The <b>DestroyPrivateObjectSecurity</b> function deletes a private object's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>. For background information, see the <a href="https://msdn.microsoft.com/f40c4b62-a3f0-4e66-875e-2ef904d052e5">Security Descriptors for Private Objects</a> topic.


## -parameters




### -param ObjectDescriptor [in, out]

A pointer to a pointer to the 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure to be deleted. This security descriptor must have been created by a call to the 
<a href="https://msdn.microsoft.com/5f4832b6-5cf5-4050-9e20-56674f2e2cb1">CreatePrivateObjectSecurity</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="authorization_functions.htm">Client/Server Access Control Functions</a>



<a href="https://msdn.microsoft.com/8301ed4f-9458-410b-af19-4f055656005a">Client/Server Access Control Overview</a>



<a href="https://msdn.microsoft.com/5f4832b6-5cf5-4050-9e20-56674f2e2cb1">CreatePrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/3e93c0a0-e449-4df1-812b-c3fb0dfe9c19">GetPrivateObjectSecurity</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/f40c4b62-a3f0-4e66-875e-2ef904d052e5">Security Descriptors for Private Objects</a>



<a href="https://msdn.microsoft.com/726994c8-7813-4f1a-b7d7-a25e79202c33">SetPrivateObjectSecurity</a>
 

 

