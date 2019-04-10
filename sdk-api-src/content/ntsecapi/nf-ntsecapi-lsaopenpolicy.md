---
UID: NF:ntsecapi.LsaOpenPolicy
title: LsaOpenPolicy function (ntsecapi.h)
author: windows-sdk-content
description: Opens a handle to the Policy object on a local or remote system.
old-location: security\lsaopenpolicy.htm
tech.root: SecAuthN
ms.assetid: 361bc962-1e97-4606-a835-cbce37692c55
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LsaOpenPolicy, LsaOpenPolicy function [Security], _lsa_lsaopenpolicy, ntsecapi/LsaOpenPolicy, security.lsaopenpolicy
ms.topic: function
req.header: ntsecapi.h
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
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaOpenPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LsaOpenPolicy function


## -description


The <b>LsaOpenPolicy</b> function opens a handle to the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object on a local or remote system.

You must run the process "As Administrator" so that the call doesn't fail with ERROR_ACCESS_DENIED.


## -parameters




### -param SystemName [in]

A pointer to an 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the name of the target system. The name can have the form "<i>ComputerName</i>" or "\\<i>ComputerName</i>". If this parameter is <b>NULL</b>, the function opens the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object on the local system.


### -param ObjectAttributes [in]

A pointer to an 
<a href="https://msdn.microsoft.com/ad05cb52-8e58-46a9-b3e8-0c9c2a24a997">LSA_OBJECT_ATTRIBUTES</a> structure that specifies the connection attributes. The structure members are not used; initialize them to <b>NULL</b> or zero.


### -param DesiredAccess [in]

An <a href="https://msdn.microsoft.com/f115ee54-3333-4109-8004-d71904a7a943">ACCESS_MASK</a> that specifies the requested access rights. The function fails if the DACL of the target system does not allow the caller the requested access. To determine the access rights that you need, see the documentation for the LSA functions with which you want to use the policy handle.


### -param PolicyHandle [in, out]

A pointer to an 
<a href="https://msdn.microsoft.com/f5878d27-558b-4ef1-9401-1277e740c61d">LSA_HANDLE</a> variable that receives a handle to the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object.

When you no longer need this handle, pass it to the 
<a href="https://msdn.microsoft.com/6283b1da-4ec3-48e1-91f6-321c6390befe">LsaClose</a> function to close it.


## -returns



If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> code. For more information, see 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> code to a Windows error code.




## -remarks



To administer the local security policy of a local or remote system, you must call the <b>LsaOpenPolicy</b> function to establish a session with that system's LSA subsystem. <b>LsaOpenPolicy</b> connects to the LSA of the target system and returns a handle to the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object of that system. You can use this handle in subsequent LSA function calls to administer the 
<a href="https://msdn.microsoft.com/9cef073f-a38f-4808-8dc9-3fabc3413eb2">local security policy</a> information of the target system.

For an example that demonstrates calling this function see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5878d27-558b-4ef1-9401-1277e740c61d">LSA_HANDLE</a>



<a href="https://msdn.microsoft.com/ad05cb52-8e58-46a9-b3e8-0c9c2a24a997">LSA_OBJECT_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/6283b1da-4ec3-48e1-91f6-321c6390befe">LsaClose</a>



<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a>
 

 

