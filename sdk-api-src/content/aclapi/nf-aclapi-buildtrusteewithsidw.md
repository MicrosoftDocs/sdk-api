---
UID: NF:aclapi.BuildTrusteeWithSidW
title: BuildTrusteeWithSidW function
author: windows-sdk-content
description: Initializes a TRUSTEE structure. The caller specifies the security identifier (SID) of the trustee. The function sets other members of the structure to default values and does not look up the name associated with the SID.
old-location: security\buildtrusteewithsid.htm
tech.root: secauthz
ms.assetid: 3745fbf2-911a-4cb6-81a8-6256c742c700
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: BuildTrusteeWithSid, BuildTrusteeWithSid function [Security], BuildTrusteeWithSidA, BuildTrusteeWithSidW, MultipleTrusteeOperation, TrusteeForm, TrusteeType, _win32_buildtrusteewithsid, aclapi/BuildTrusteeWithSid, aclapi/BuildTrusteeWithSidA, aclapi/BuildTrusteeWithSidW, pMultipleTrustee, security.buildtrusteewithsid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: BuildTrusteeWithSidW (Unicode) and BuildTrusteeWithSidA (ANSI)
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
 - API-MS-Win-security-trustee-l1-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-security-trustee-l1-1-1.dll
api_name:
 - BuildTrusteeWithSid
 - BuildTrusteeWithSidA
 - BuildTrusteeWithSidW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BuildTrusteeWithSidW function


## -description


The <b>BuildTrusteeWithSid</b> function initializes a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure. The caller specifies the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the trustee. The function sets other members of the structure to default values and does not look up the name associated with the SID.


## -parameters




### -param pTrustee [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure to initialize. The <b>BuildTrusteeWithSid</b> function does not allocate any memory. If this parameter is <b>NULL</b> or a pointer that is not valid, the results are undefined.


### -param pSid [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that identifies the trustee. The <b>BuildTrusteeWithSid</b> function assigns this pointer to the <b>ptstrName</b> member of the <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure. The function sets the other members of the <b>TRUSTEE</b> structure as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="pMultipleTrustee"></a><a id="pmultipletrustee"></a><a id="PMULTIPLETRUSTEE"></a><dl>
<dt><b><b>pMultipleTrustee</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b>

</td>
</tr>
<tr>
<td width="40%"><a id="MultipleTrusteeOperation"></a><a id="multipletrusteeoperation"></a><a id="MULTIPLETRUSTEEOPERATION"></a><dl>
<dt><b><b>MultipleTrusteeOperation</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
NO_MULTIPLE_TRUSTEE

</td>
</tr>
<tr>
<td width="40%"><a id="TrusteeForm"></a><a id="trusteeform"></a><a id="TRUSTEEFORM"></a><dl>
<dt><b><b>TrusteeForm</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
TRUSTEE_IS_SID

</td>
</tr>
<tr>
<td width="40%"><a id="TrusteeType"></a><a id="trusteetype"></a><a id="TRUSTEETYPE"></a><dl>
<dt><b><b>TrusteeType</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
TRUSTEE_IS_UNKNOWN

</td>
</tr>
</table>
 


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/a66c23ac-8211-40fd-bfe8-ef9089bf3745">BuildTrusteeWithName</a>



<a href="https://msdn.microsoft.com/62edadfe-0a7b-43ec-bd02-a63f928c7618">BuildTrusteeWithObjectsAndName</a>



<a href="https://msdn.microsoft.com/e940a87f-013e-458c-bdc1-9e81c7d905e0">BuildTrusteeWithObjectsAndSid</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 

