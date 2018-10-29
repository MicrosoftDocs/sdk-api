---
UID: NF:securitybaseapi.MakeAbsoluteSD
title: MakeAbsoluteSD function
author: windows-sdk-content
description: Creates a security descriptor in absolute format by using a security descriptor in self-relative format as a template.
old-location: security\makeabsolutesd.htm
tech.root: SecAuthZ
ms.assetid: 47c75071-f10d-43cf-a841-2dd49fc39afa
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: MakeAbsoluteSD, MakeAbsoluteSD function [Security], _win32_makeabsolutesd, security.makeabsolutesd, securitybaseapi/MakeAbsoluteSD
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - MakeAbsoluteSD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MakeAbsoluteSD function


## -description


The <b>MakeAbsoluteSD</b> function creates a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> in <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">absolute</a> format by using a security descriptor in <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">self-relative</a> format as a template.


## -parameters




### -param pSelfRelativeSecurityDescriptor [in]

A pointer to a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure in self-relative format. The function creates an absolute-format version of this security descriptor without modifying the original security descriptor.


### -param pAbsoluteSecurityDescriptor [out, optional]

A pointer to a buffer that the function fills with the main body of an absolute-format security descriptor. This information is formatted as a <a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure.


### -param lpdwAbsoluteSecurityDescriptorSize [in, out]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>pAbsoluteSD</i> parameter. If the buffer is not large enough for the security descriptor, the function fails and sets this variable to the minimum required size.


### -param pDacl [out, optional]

A pointer to a buffer the function fills with the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) of the absolute-format security descriptor. The main body of the absolute-format security descriptor references this pointer.


### -param lpdwDaclSize [in, out]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>pDacl</i> parameter. If the buffer is not large enough for the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL), the function fails and sets this variable to the minimum required size.


### -param pSacl [out, optional]

A pointer to a buffer the function fills with the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) of the absolute-format security descriptor. The main body of the absolute-format security descriptor references this pointer.


### -param lpdwSaclSize [in, out]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>pSacl</i> parameter. If the buffer is not large enough for the ACL, the function fails and sets this variable to the minimum required size.


### -param pOwner [out, optional]

A pointer to a buffer the function fills with the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the owner of the absolute-format security descriptor. The main body of the absolute-format security descriptor references this pointer.


### -param lpdwOwnerSize [in, out]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>pOwner</i> parameter. If the buffer is not large enough for the SID, the function fails and sets this variable to the minimum required size.


### -param pPrimaryGroup [out, optional]

A pointer to a buffer the function fills with the SID of the absolute-format security descriptor's primary group. The main body of the absolute-format security descriptor references this pointer.


### -param lpdwPrimaryGroupSize [in, out]

A pointer to a variable that specifies the size of the buffer pointed to by the <i>pPrimaryGroup</i> parameter. If the buffer is not large enough for the SID, the function fails and sets this variable to the minimum required size.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible return codes include, but are not limited to, the following.



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



A security descriptor in absolute format contains pointers to the information it contains, rather than the information itself. A security descriptor in self-relative format contains the information in a contiguous block of memory. In a self-relative security descriptor, a 
<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a> structure always starts the information, but the security descriptor's other components can follow the structure in any order. Instead of using memory addresses, the components of the self-relative security descriptor are identified by offsets from the beginning of the security descriptor. This format is useful when a security descriptor must be stored on a floppy disk or transmitted by means of a communications protocol.

A server that copies secured objects to various media can use the <b>MakeAbsoluteSD</b> function to create an absolute security descriptor from a self-relative security descriptor and the 
<a href="https://msdn.microsoft.com/497c7e2f-75b7-41b9-9693-37e041b7af58">MakeSelfRelativeSD</a> function to create a self-relative security descriptor from an absolute security descriptor.




## -see-also




<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/497c7e2f-75b7-41b9-9693-37e041b7af58">MakeSelfRelativeSD</a>



<a href="https://msdn.microsoft.com/653992aa-4e32-4187-b3ac-727e82bfe0b6">SECURITY_DESCRIPTOR</a>
 

 

