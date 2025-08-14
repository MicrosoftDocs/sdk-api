---
UID: NF:securitybaseapi.GetSecurityDescriptorRMControl
title: GetSecurityDescriptorRMControl function (securitybaseapi.h)
description: Retrieves the resource manager control bits.
helpviewer_keywords: ["GetSecurityDescriptorRMControl","GetSecurityDescriptorRMControl function [Security]","_win32_getsecuritydescriptorrmcontrol","security.getsecuritydescriptorrmcontrol","securitybaseapi/GetSecurityDescriptorRMControl"]
old-location: security\getsecuritydescriptorrmcontrol.htm
tech.root: security
ms.assetid: a1e2ce12-586b-4011-a82d-e246d5544367
ms.date: 12/05/2018
ms.keywords: GetSecurityDescriptorRMControl, GetSecurityDescriptorRMControl function [Security], _win32_getsecuritydescriptorrmcontrol, security.getsecuritydescriptorrmcontrol, securitybaseapi/GetSecurityDescriptorRMControl
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetSecurityDescriptorRMControl
 - securitybaseapi/GetSecurityDescriptorRMControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - GetSecurityDescriptorRMControl
---

# GetSecurityDescriptorRMControl function


## -description

The <b>GetSecurityDescriptorRMControl</b> function retrieves the <a href="/windows/desktop/SecGloss/r-gly">resource manager</a> control bits.

## -parameters

### -param SecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that contains the <a href="/windows/desktop/SecGloss/r-gly">resource manager</a> control bits. The value of the <b>Control</b> member is set to SE_RM_CONTROL_VALID.

### -param RMControl [out]

A pointer to a buffer that receives the resource manager control bits.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the following value is returned.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The SE_RM_CONTROL_VALID bit flag is not set in the specified 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure.

</td>
</tr>
</table>

## -remarks

The <a href="/windows/desktop/SecGloss/r-gly">resource manager</a> control bits are eight bits in the <b>Sbz1</b> member of the <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure that contains information specific to the resource manager accessing the structure. These bits should be accessed only through the <b>GetSecurityDescriptorRMControl</b> and 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorrmcontrol">SetSecurityDescriptorRMControl</a> functions.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorrmcontrol">SetSecurityDescriptorRMControl</a>