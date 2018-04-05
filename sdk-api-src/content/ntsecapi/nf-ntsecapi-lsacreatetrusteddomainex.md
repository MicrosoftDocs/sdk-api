---
UID: NF:ntsecapi.LsaCreateTrustedDomainEx
title: LsaCreateTrustedDomainEx function
author: windows-driver-content
description: The LsaCreateTrustedDomainEx function establishes a new trusted domain by creating a new TrustedDomain object.
old-location: security\lsacreatetrusteddomainex.htm
old-project: SecMgmt
ms.assetid: 2f458098-9498-4f08-bd13-ac572678d734
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: LsaCreateTrustedDomainEx, LsaCreateTrustedDomainEx function [Security], _lsa_lsacreatetrusteddomainex, ntsecapi/LsaCreateTrustedDomainEx, security.lsacreatetrusteddomainex
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	LsaCreateTrustedDomainEx
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# LsaCreateTrustedDomainEx function


## -description


The <b>LsaCreateTrustedDomainEx</b> function establishes a new trusted domain by creating a new <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> object.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. For the object to be created, the caller must have permission to create children on the <b>System</b> container. For information about policy object handles, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param TrustedDomainInformation [in]

Pointer to a 
<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a> structure that contains the name and SID of the new trusted domain.


### -param AuthenticationInformation [in]

Pointer to a 
<a href="https://msdn.microsoft.com/2ec606d7-42bd-47cc-a4cd-82908774aa43">TRUSTED_DOMAIN_AUTH_INFORMATION</a> structure that contains authentication information for the new trusted domain.


### -param DesiredAccess [in]

An 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> structure that specifies the accesses to be granted for the new trusted domain.


### -param TrustedDomainHandle [out]

Receives the LSA policy handle of the remote trusted domain. You can pass this handle into LSA function calls to manage the LSA policy of the trusted domain. 




When your application no longer needs this handle, it should call 
<a href="https://msdn.microsoft.com/6283b1da-4ec3-48e1-91f6-321c6390befe">LsaClose</a> to delete the handle.


## -returns



If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> code, which can be one of the following values or one of the 
<a href="management_return_values.htm">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_DIRECTORY_SERVICE_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
 The target system (specified in the <i>TrustedDomainInformation</i> parameter) for the <a href="https://msdn.microsoft.com/fab69367-2143-49ef-a1b9-9c1d846fd4e1">TrustedDomain</a> object is not a domain controller.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_SID</b></dt>
</dl>
</td>
<td width="60%">
The specified SID is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_UNSUCCESSFUL</b></dt>
</dl>
</td>
<td width="60%">
Unable to determine whether the target system is a domain controller.

</td>
</tr>
</table>
 

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the <b>NTSTATUS</b> code to a Windows error code.




## -remarks



<b>LsaCreateTrustedDomainEx</b> does not check whether the specified domain name matches the specified SID or whether the SID and name represent an actual domain.




## -see-also




<a href="https://msdn.microsoft.com/6283b1da-4ec3-48e1-91f6-321c6390befe">LsaClose</a>



<a href="https://msdn.microsoft.com/4a7afa28-1786-4a58-a955-d2d8b12e62e4">LsaDeleteTrustedDomain</a>



<a href="https://msdn.microsoft.com/263e1025-1010-463d-8bc7-cdf916ce9872">LsaSetTrustedDomainInfoByName</a>



<a href="https://msdn.microsoft.com/a7b89ea7-af92-46ba-ac73-2fba1cc27680">LsaSetTrustedDomainInformation</a>



<a href="https://msdn.microsoft.com/2ec606d7-42bd-47cc-a4cd-82908774aa43">TRUSTED_DOMAIN_AUTH_INFORMATION</a>



<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a>
 

 

