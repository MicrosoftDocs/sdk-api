---
UID: NF:securitybaseapi.IsValidAcl
title: IsValidAcl function
author: windows-sdk-content
description: Validates an access control list (ACL).
old-location: security\isvalidacl.htm
tech.root: SecAuthZ
ms.assetid: 3ae9f147-4e90-44df-a1af-cf6ebad92aea
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IsValidAcl, IsValidAcl function [Security], _win32_isvalidacl, security.isvalidacl, securitybaseapi/IsValidAcl
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
 - IsValidAcl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsValidAcl function


## -description


The <b>IsValidAcl</b> function validates an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL).


## -parameters




### -param pAcl [in]

A pointer to an
      <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure validated by this function. This value must not be <b>NULL</b>.


## -returns



If the ACL is valid, the function returns nonzero.
      

If the ACL is not valid, the function returns zero. There is no extended error information for this function; do not call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function checks the revision level of the ACL and verifies that the number of <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) specified in the <b>AceCount</b> member of the <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure fits the space specified by the <b>AclSize</b> member of the <b>ACL</b> structure.

If <i>pAcl</i> is <b>NULL</b>, the application will fail with an access violation.




## -see-also




<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/23ef6abd-03e9-439e-ba05-629c8d61cd66">GetAclInformation</a>



<a href="https://msdn.microsoft.com/b990a7bd-7840-4c10-baf8-68b3862147f4">InitializeAcl</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>
 

 

