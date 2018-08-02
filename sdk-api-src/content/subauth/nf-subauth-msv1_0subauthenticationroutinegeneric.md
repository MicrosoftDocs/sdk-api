---
UID: NF:subauth.Msv1_0SubAuthenticationRoutineGeneric
title: Msv1_0SubAuthenticationRoutineGeneric function
author: windows-sdk-content
description: Performs Remote Access Service authentication when subauthentication is requested by calling the LsaCallAuthenticationPackage function.
old-location: security\msv1_0subauthenticationroutinegeneric.htm
old-project: SecAuthN
ms.assetid: 78F51B69-DCFA-47D0-84C5-B44C79D50DAF
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Msv1_0SubAuthenticationRoutineGeneric, Msv1_0SubAuthenticationRoutineGeneric function [Security], security.msv1_0subauthenticationroutinegeneric, subauth/Msv1_0SubAuthenticationRoutineGeneric
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: subauth.h
req.include-header: 
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
tech.root: 
req.typenames: CONDITION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Subauth.h
api_name:
 - Msv1_0SubAuthenticationRoutineGeneric
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# Msv1_0SubAuthenticationRoutineGeneric function


## -description


Performs <a href="https://msdn.microsoft.com/fa0a183a-0254-401e-8b78-441cb3f83e8b">Remote Access Service</a> authentication when subauthentication is requested by calling the <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> function.

The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security principal's</a> credentials and information from the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security Accounts Manager</a> (SAM) database are passed to this function for authentication.

This function is implemented by custom subauthentication package DLLs for use with the MSV1_0 authentication package.

This function is called only for a 
<a href="https://msdn.microsoft.com/1539cbfa-d84f-4989-8380-6cfc7c496310">noninteractive authentication</a>, only on the authenticating server where the account resides, and only if a subauthentication DLL is registered under the correct key in the registry.


## -parameters




### -param SubmitBuffer

A pointer to a buffer that contains a <a href="https://msdn.microsoft.com/5a408c0a-56d4-48f6-8289-6f203ef998df">MSV1_0_SUBAUTH_REQUEST</a> structure that contains the  authentication information to be submitted.


### -param SubmitBufferLength

The  size, in bytes, of the <i>SubmitBuffer</i> buffer.


### -param ReturnBufferLength [out]

The size, in bytes, of the <i>ReturnBuffer</i> buffer.


### -param ReturnBuffer [out]

A pointer to a buffer that contains a <a href="https://msdn.microsoft.com/62808fba-6e10-4f3b-a705-6958fc4fe480">MSV1_0_SUBAUTH_RESPONSE</a> structure that contains the response from the subauthentication package.


## -returns



If the function succeeds, the return value is <b>STATUS_SUCCESS</b>.

If the function fails, the return value is an NTSTATUS code.




## -see-also




<a href="https://msdn.microsoft.com/18d0da59-026a-4951-8529-f7dbaab20d08">Msv1_0SubAuthenticationRoutine</a>
 

 

