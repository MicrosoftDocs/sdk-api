---
UID: NF:ntsecapi.LsaOpenTrustedDomainByName
title: LsaOpenTrustedDomainByName function
author: windows-sdk-content
description: The LsaOpenTrustedDomainByName function opens the LSA policy handle of a remote trusted domain. You can pass this handle into LSA function calls in order to set or query the LSA policy of the remote machine.
old-location: security\lsaopentrusteddomainbyname.htm
old-project: SecMgmt
ms.assetid: 6c55f8b4-d8a2-48e3-8074-b3ca22ce487a
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: LsaOpenTrustedDomainByName, LsaOpenTrustedDomainByName function [Security], _lsa_lsaopentrusteddomainbyname, ntsecapi/LsaOpenTrustedDomainByName, security.lsaopentrusteddomainbyname
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
api_name:
-	LsaOpenTrustedDomainByName
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LsaOpenTrustedDomainByName function


## -description


The <b>LsaOpenTrustedDomainByName</b> function opens the LSA policy handle of a remote trusted domain. You can pass this handle into LSA function calls in order to set or query the LSA policy of the remote machine.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. This is the policy handle of the local machine. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param TrustedDomainName [in]

Name of the trusted domain. This name can be either the flat name, or the Domain Name System (DNS) domain name.


### -param DesiredAccess [in]

An 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> structure that specifies the access permissions requested on the remote trusted domain object.


### -param TrustedDomainHandle [out]

Pointer that receives the address of the LSA policy handle of the remote trusted domain. You can pass this handle into LSA function calls in order to query and manage the LSA policy of the remote machine. 




When your application no longer needs this handle, it should call 
<a href="https://msdn.microsoft.com/6283b1da-4ec3-48e1-91f6-321c6390befe">LsaClose</a> to delete the handle.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be one of the following values or one of the 
<a href="management_return_values.htm">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Caller does not have the appropriate access to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_OBJECT_NAME_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
There is no Trusted Domain object in the target system's LSA Database having the specified name.

</td>
</tr>
</table>
 

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/6283b1da-4ec3-48e1-91f6-321c6390befe">LsaClose</a>
 

 

