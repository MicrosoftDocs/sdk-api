---
UID: NF:securitybaseapi.AllocateAndInitializeSid
title: AllocateAndInitializeSid function
author: windows-sdk-content
description: Allocates and initializes a security identifier (SID) with up to eight subauthorities.
old-location: security\allocateandinitializesid.htm
tech.root: SecAuthZ
ms.assetid: fcdff2f8-7f43-4c0f-b548-4914b1991937
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: AllocateAndInitializeSid, AllocateAndInitializeSid function [Security], _win32_allocateandinitializesid, security.allocateandinitializesid, securitybaseapi/AllocateAndInitializeSid
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
 - AllocateAndInitializeSid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AllocateAndInitializeSid function


## -description


The <b>AllocateAndInitializeSid</b> function allocates and initializes a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) with up to eight subauthorities.


## -parameters




### -param pIdentifierAuthority [in]

A pointer to a 
<a href="https://msdn.microsoft.com/450a6d2d-d2e4-4098-90af-a8024ddcfcb5">SID_IDENTIFIER_AUTHORITY</a> structure. This structure provides the top-level identifier authority value to set in the SID.


### -param nSubAuthorityCount [in]

Specifies the number of subauthorities to place in the SID. This parameter also identifies how many of the subauthority parameters have meaningful values. This parameter must contain a value from 1 to 8. 




For example, a value of 3 indicates that the subauthority values specified by the <i>dwSubAuthority0</i>, <i>dwSubAuthority1</i>, and <i>dwSubAuthority2</i> parameters have meaningful values and to ignore the remainder.


### -param nSubAuthority0 [in]

Subauthority value to place in the SID.


### -param nSubAuthority1 [in]

Subauthority value to place in the SID.


### -param nSubAuthority2 [in]

Subauthority value to place in the SID.


### -param nSubAuthority3 [in]

Subauthority value to place in the SID.


### -param nSubAuthority4 [in]

Subauthority value to place in the SID.


### -param nSubAuthority5 [in]

Subauthority value to place in the SID.


### -param nSubAuthority6 [in]

Subauthority value to place in the SID.


### -param nSubAuthority7 [in]

Subauthority value to place in the SID.


### -param pSid [out]

A pointer to a variable that receives the pointer to the allocated and initialized 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A SID allocated with the <b>AllocateAndInitializeSid</b> function must be freed by using the <a href="https://msdn.microsoft.com/1e2098d8-4d1f-4353-97c1-549021a5b3fd">FreeSid</a> function.

This function creates a SID with a 32-bit RID value. For applications that require longer RID values, use 
<a href="https://msdn.microsoft.com/00e75bae-fbce-41a3-a0bc-c345c36f2c84">CreateWellKnownSid</a>.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/866992a7-95c4-4094-87bb-e6d8eeb24317">Creating a Security Descriptor for a New Object</a> or <a href="https://msdn.microsoft.com/0b309ac9-177d-425f-8b78-71fe73e41979">Taking Object Ownership</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/1e2098d8-4d1f-4353-97c1-549021a5b3fd">FreeSid</a>



<a href="https://msdn.microsoft.com/67a06e7b-775f-424c-ab36-0fc9b93b801a">GetSidIdentifierAuthority</a>



<a href="https://msdn.microsoft.com/b2d803a5-faaf-4066-ba2c-0442c71bb150">InitializeSid</a>



<a href="https://msdn.microsoft.com/450a6d2d-d2e4-4098-90af-a8024ddcfcb5">SID_IDENTIFIER_AUTHORITY</a>



<a href="https://msdn.microsoft.com/eb2f95c4-9465-409b-b76c-9ccae1d05eda">Well-known SIDs</a>
 

 

