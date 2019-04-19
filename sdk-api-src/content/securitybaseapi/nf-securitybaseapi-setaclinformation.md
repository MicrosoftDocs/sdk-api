---
UID: NF:securitybaseapi.SetAclInformation
title: SetAclInformation function (securitybaseapi.h)
author: windows-sdk-content
description: Sets information about an access control list (ACL).
old-location: security\setaclinformation.htm
tech.root: SecAuthZ
ms.assetid: bb4dd7f9-2f15-4a27-89c9-1675f4fb8d92
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetAclInformation, SetAclInformation function [Security], _win32_setaclinformation, security.setaclinformation, securitybaseapi/SetAclInformation
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - SetAclInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetAclInformation function


## -description


The <b>SetAclInformation</b> function sets information about an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL).


## -parameters




### -param pAcl [in, out]

A pointer to an 
ACL. The function sets information in this ACL.


### -param pAclInformation [in]

A pointer to a buffer that contains the information to be set. This must be a pointer to an 
<a href="https://msdn.microsoft.com/cdc7f6b1-aaa1-4893-a192-5a42233b3ec1">ACL_REVISION_INFORMATION</a> structure.


### -param nAclInformationLength [in]

The size, in bytes, of the buffer pointed to by the <i>pAclInfo</i> parameter.


### -param dwAclInformationClass [in]

An 
<a href="https://msdn.microsoft.com/e1abf877-9757-4ee4-b7da-f3e7eb53bddd">ACL_INFORMATION_CLASS</a> enumerated type that gives the class of information requested. 




Currently, this parameter can be <b>AclRevisionInformation</b>. This means that the buffer pointed to by the <i>pAclInformation</i> parameter contains an 
<a href="https://msdn.microsoft.com/cdc7f6b1-aaa1-4893-a192-5a42233b3ec1">ACL_REVISION_INFORMATION</a> structure.


## -returns



If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/e1abf877-9757-4ee4-b7da-f3e7eb53bddd">ACL_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/cdc7f6b1-aaa1-4893-a192-5a42233b3ec1">ACL_REVISION_INFORMATION</a>



<a href="https://msdn.microsoft.com/23ef6abd-03e9-439e-ba05-629c8d61cd66">GetAclInformation</a>



<a href="https://msdn.microsoft.com/b990a7bd-7840-4c10-baf8-68b3862147f4">InitializeAcl</a>



<a href="https://msdn.microsoft.com/3ae9f147-4e90-44df-a1af-cf6ebad92aea">IsValidAcl</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Low-level Access Control Functions</a>
 

 

