---
UID: NF:securitybaseapi.GetAclInformation
title: GetAclInformation function
author: windows-sdk-content
description: Retrieves information about an access control list (ACL).
old-location: security\getaclinformation.htm
tech.root: SecAuthZ
ms.assetid: 23ef6abd-03e9-439e-ba05-629c8d61cd66
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetAclInformation, GetAclInformation function [Security], _win32_getaclinformation, security.getaclinformation, securitybaseapi/GetAclInformation
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
 - GetAclInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetAclInformation function


## -description


The <b>GetAclInformation</b> function retrieves information about an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL).


## -parameters




### -param pAcl [in]

A pointer to an 
ACL. The function retrieves information about this ACL. If a null value is passed, the function causes an access violation.


### -param pAclInformation [out]

A pointer to a buffer to receive the requested information. The structure that is placed into the buffer depends on the information class requested in the <i>dwAclInformationClass</i> parameter.


### -param nAclInformationLength [in]

The size, in bytes, of the buffer pointed to by the <i>pAclInformation</i> parameter.


### -param dwAclInformationClass [in]

A value of the 
<a href="https://msdn.microsoft.com/e1abf877-9757-4ee4-b7da-f3e7eb53bddd">ACL_INFORMATION_CLASS</a> enumeration that indicates the class of information requested. This parameter can be one of two values from this enumeration:

<ul>
<li>If the value is <b>AclRevisionInformation</b>, the function fills the buffer pointed to by the <i>pAclInformation</i> parameter with an 
<a href="https://msdn.microsoft.com/cdc7f6b1-aaa1-4893-a192-5a42233b3ec1">ACL_REVISION_INFORMATION</a> structure.</li>
<li>If the value is <b>AclSizeInformation</b>, the function fills the buffer pointed to by the <i>pAclInformation</i> parameter with an 
<a href="https://msdn.microsoft.com/05034096-211d-4ee3-a686-dfebfa167814">ACL_SIZE_INFORMATION</a> structure.</li>
</ul>

## -returns



If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/e1abf877-9757-4ee4-b7da-f3e7eb53bddd">ACL_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/cdc7f6b1-aaa1-4893-a192-5a42233b3ec1">ACL_REVISION_INFORMATION</a>



<a href="https://msdn.microsoft.com/05034096-211d-4ee3-a686-dfebfa167814">ACL_SIZE_INFORMATION</a>



<a href="https://msdn.microsoft.com/5b5d8751-20d7-40a2-bd70-cfbe956aaa03">GetAce</a>



<a href="https://msdn.microsoft.com/b990a7bd-7840-4c10-baf8-68b3862147f4">InitializeAcl</a>



<a href="https://msdn.microsoft.com/3ae9f147-4e90-44df-a1af-cf6ebad92aea">IsValidAcl</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/bb4dd7f9-2f15-4a27-89c9-1675f4fb8d92">SetAclInformation</a>
 

 

