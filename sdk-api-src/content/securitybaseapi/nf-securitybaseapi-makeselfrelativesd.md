---
UID: NF:securitybaseapi.MakeSelfRelativeSD
title: MakeSelfRelativeSD function (securitybaseapi.h)
description: Creates a security descriptor in self-relative format by using a security descriptor in absolute format as a template.
helpviewer_keywords: ["MakeSelfRelativeSD","MakeSelfRelativeSD function [Security]","_win32_makeselfrelativesd","security.makeselfrelativesd","securitybaseapi/MakeSelfRelativeSD"]
old-location: security\makeselfrelativesd.htm
tech.root: security
ms.assetid: 497c7e2f-75b7-41b9-9693-37e041b7af58
ms.date: 12/05/2018
ms.keywords: MakeSelfRelativeSD, MakeSelfRelativeSD function [Security], _win32_makeselfrelativesd, security.makeselfrelativesd, securitybaseapi/MakeSelfRelativeSD
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
 - MakeSelfRelativeSD
 - securitybaseapi/MakeSelfRelativeSD
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
 - MakeSelfRelativeSD
---

# MakeSelfRelativeSD function


## -description

The <b>MakeSelfRelativeSD</b> function creates a <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a> in <a href="/windows/desktop/SecGloss/s-gly">self-relative</a> format by using a security descriptor in <a href="/windows/desktop/SecGloss/a-gly">absolute</a> format as a template.

## -parameters

### -param pAbsoluteSecurityDescriptor [in]

A pointer to a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure in absolute format. The function creates a version of this security descriptor in self-relative format without modifying the original.

### -param pSelfRelativeSecurityDescriptor [out, optional]

A pointer to a buffer the function fills with a security descriptor in self-relative format.

### -param lpdwBufferLength [in, out]

A pointer to a variable specifying the size of the buffer pointed to by the <i>pSelfRelativeSD</i> parameter. If the buffer is not large enough for the security descriptor, the function fails and sets this variable to the minimum required size.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.  Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
<dt>0x7A</dt>
</dl>
</td>
<td width="60%">
One or more of the buffers is too small.

</td>
</tr>
</table>

## -remarks

A security descriptor in absolute format contains pointers to the information it contains, rather than containing the information itself. A security descriptor in self-relative format contains the information in a contiguous block of memory. In a self-relative security descriptor, a 
<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> structure always starts the information, but the security descriptor's other components can follow the structure in any order. Instead of using memory addresses, the components of the security descriptor are identified by offsets from the beginning of the security descriptor. This format is useful when a security descriptor must be stored on a floppy disk or transmitted by means of a communications protocol.

A server that copies secured objects to various media can use the <b>MakeSelfRelativeSD</b> function to create a self-relative security descriptor from an absolute security descriptor and the 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd">MakeAbsoluteSD</a> function to create an absolute security descriptor from a self-relative security descriptor.

## -see-also

<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-makeabsolutesd">MakeAbsoluteSD</a>



<a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a>