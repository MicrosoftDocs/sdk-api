---
UID: NF:securitybaseapi.QuerySecurityAccessMask
title: QuerySecurityAccessMask function (securitybaseapi.h)
author: windows-sdk-content
description: Creates an access mask that represents the access permissions necessary to query the specified object security information.
old-location: security\querysecurityaccessmask.htm
tech.root: SecAuthZ
ms.assetid: 70379640-28b7-4503-9ba8-789786078d4a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: QuerySecurityAccessMask, QuerySecurityAccessMask function [Security], security.querysecurityaccessmask, securitybaseapi/QuerySecurityAccessMask, winbase/QuerySecurityAccessMask
ms.topic: function
req.header: securitybaseapi.h
req.include-header: WinBase.h
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
 - QuerySecurityAccessMask
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# QuerySecurityAccessMask function


## -description


The <b>QuerySecurityAccessMask</b> function creates an access mask that represents the access permissions necessary to query the specified object security information.


## -parameters




### -param SecurityInformation [in]

A <a href="https://msdn.microsoft.com/e3e8b35d-9d18-4611-a898-72ca13e40d33">SECURITY_INFORMATION</a> structure that specifies the security information to be queried.


### -param DesiredAccess [out]

A pointer to the access mask that this function creates.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/764a4e93-0865-49f8-9b3a-1a178073454d">SetSecurityAccessMask</a>
 

 

