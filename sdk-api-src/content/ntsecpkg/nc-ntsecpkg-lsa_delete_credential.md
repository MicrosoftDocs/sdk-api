---
UID: NC:ntsecpkg.LSA_DELETE_CREDENTIAL
title: LSA_DELETE_CREDENTIAL
author: windows-driver-content
description: Deletes an existing credential.
old-location: security\deletecredential.htm
old-project: SecAuthN
ms.assetid: 06bc02ec-5c07-41db-9f00-49773a597a09
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: DeleteCredential, DeleteCredential function [Security], LSA_DELETE_CREDENTIAL, _lsa_deletecredential, ntsecpkg/DeleteCredential, security.deletecredential
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ntsecpkg.h
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	DeleteCredential
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_DELETE_CREDENTIAL callback function


## -description


Deletes an existing credential.

This function deletes the first credential it finds with a matching logon session ID, authentication package ID, and primary lookup key value. If there are multiple matching credentials, only one of them is deleted.

This function is not used by newer authentication packages, such as Kerberos.


## -parameters




### -param LogonId [in]

Pointer to an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> structure containing the session ID of the logon session from which the credential is to be deleted.


### -param AuthenticationPackage [in]

Authentication package ID of the calling authentication package received in the 
<a href="https://msdn.microsoft.com/1fed5a5e-5dc1-4b59-aa28-bd1395a27742">LsaApInitializePackage</a> call during DLL initialization.


### -param PrimaryKeyValue [in]

Contains the primary lookup key of the credential to be deleted.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be one of the following values or one of the 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GEN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
No matching credential could be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_NO_SUCH_LOGON_SESSION</b></dt>
</dl>
</td>
<td width="60%">
The specified logon session could not be found.

</td>
</tr>
</table>
 

The 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function converts an NTSTATUS code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/2e144ce0-e8c9-457a-8b12-7d21dda6adf3">LSA_DISPATCH_TABLE</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>
 

 

