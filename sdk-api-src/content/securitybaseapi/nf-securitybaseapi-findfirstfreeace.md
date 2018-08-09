---
UID: NF:securitybaseapi.FindFirstFreeAce
title: FindFirstFreeAce function
author: windows-sdk-content
description: Retrieves a pointer to the first free byte in an access control list (ACL).
old-location: security\findfirstfreeace.htm
old-project: secauthz
ms.assetid: bf770761-008a-4a35-b31f-b781d5a8622b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FindFirstFreeAce, FindFirstFreeAce function [Security], _win32_findfirstfreeace, security.findfirstfreeace, securitybaseapi/FindFirstFreeAce
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EXTENDED_NAME_FORMAT, *PEXTENDED_NAME_FORMAT
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
 - FindFirstFreeAce
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# FindFirstFreeAce function


## -description


The <b>FindFirstFreeAce</b> function retrieves a pointer to the first free byte in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL).


## -parameters




### -param pAcl [in]

A pointer to an 
ACL.


### -param pAce [out]

The address of a pointer to the first free position in the ACL created when the function returns. If the ACL is not valid, this parameter is <b>NULL</b>. If the ACL is full, this parameter points to the byte immediately following the ACL.


## -returns



If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/5b5d8751-20d7-40a2-bd70-cfbe956aaa03">GetAce</a>



<a href="https://msdn.microsoft.com/23ef6abd-03e9-439e-ba05-629c8d61cd66">GetAclInformation</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="authorization_functions.htm">Low-level Access Control Functions</a>
 

 

