---
UID: NF:ntsecapi.AuditQuerySecurity
title: AuditQuerySecurity function
author: windows-driver-content
description: Retrieves security descriptor that delegates access to audit policy.
old-location: security\auditquerysecurity.htm
old-project: SecAuthZ
ms.assetid: 496c9659-0c03-42c9-93c4-eb4d97e950e2
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: AuditQuerySecurity, AuditQuerySecurity function [Security], ntsecapi/AuditQuerySecurity, security.auditquerysecurity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	API-MS-Win-Security-audit-l1-1-1.dll
-	sechost.dll
api_name:
-	AuditQuerySecurity
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# AuditQuerySecurity function


## -description


The <b>AuditQuerySecurity</b> function retrieves <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> that delegates access to audit policy.


## -parameters




### -param SecurityInformation [in]

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> value that specifies which parts of the security descriptor this function sets. Only <b>SACL_SECURITY_INFORMATION</b> and <b>DACL_SECURITY_INFORMATION</b> are supported. Any other values are ignored. If neither <b>SACL_SECURITY_INFORMATION</b> nor <b>DACL_SECURITY_INFORMATION</b> is specified, this function fails and returns <b>ERROR_INVALID_PARAMETER</b>.


### -param ppSecurityDescriptor [out]

The address of a pointer to a well-formed <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> structure that controls access to the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Audit security object</a>.


## -returns




						If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. <b>GetLastError</b> may return one of the following error codes defined in WinError.h.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The caller does not have the privilege or access rights necessary to call this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
<dt>87</dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 




## -remarks



To successfully call this function, the caller must have <b>SeSecurityPrivilege</b>.




## -see-also




<a href="https://msdn.microsoft.com/2f4d6198-775a-40e4-9158-a69e71bfe050">AuditSetSecurity</a>
 

 

