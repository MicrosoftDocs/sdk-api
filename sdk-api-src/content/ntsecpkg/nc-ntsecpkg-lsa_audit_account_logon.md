---
UID: NC:ntsecpkg.LSA_AUDIT_ACCOUNT_LOGON
title: LSA_AUDIT_ACCOUNT_LOGON
author: windows-driver-content
description: The AuditAccountLogon function produces an audit record that represents the mapping of a foreign principal name onto a Windows account.
old-location: security\auditaccountlogon.htm
old-project: SecAuthN
ms.assetid: dcf2d16b-8352-4d40-9723-c8cf8465431c
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: AuditAccountLogon, AuditAccountLogon function [Security], LSA_AUDIT_ACCOUNT_LOGON, _ssp_auditaccountlogon, ntsecpkg/AuditAccountLogon, security.auditaccountlogon
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
-	AuditAccountLogon
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_AUDIT_ACCOUNT_LOGON callback function


## -description


The <b>AuditAccountLogon</b> function produces an audit record that represents the mapping of a foreign <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">principal</a> name onto a Windows account.


## -parameters




### -param AuditId [in]

<a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security package</a>–defined message identifier. This value is included in the audit record.


### -param Success [in]

Specifies whether the audit record is generated on success or failure of the logon.


### -param Source [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> specifying the source of the logon attempt.


### -param ClientName [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> specifying the client name.


### -param MappedName [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the Windows account name to which the client name was mapped, if any.


### -param Status [in]

An NTSTATUS value specifying any error that occurred.


## -returns



This function returns STATUS_SUCCESS.




## -remarks



A pointer to the <b>AuditAccountLogon</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

