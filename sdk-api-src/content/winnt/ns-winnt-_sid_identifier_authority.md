---
UID: NS:winnt._SID_IDENTIFIER_AUTHORITY
title: "_SID_IDENTIFIER_AUTHORITY"
author: windows-driver-content
description: Represents the top-level authority of a security identifier (SID).
old-location: security\sid_identifier_authority.htm
old-project: SecAuthZ
ms.assetid: 450a6d2d-d2e4-4098-90af-a8024ddcfcb5
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PSID_IDENTIFIER_AUTHORITY, PSID_IDENTIFIER_AUTHORITY, PSID_IDENTIFIER_AUTHORITY structure pointer [Security], SID_IDENTIFIER_AUTHORITY, SID_IDENTIFIER_AUTHORITY structure [Security], _SID_IDENTIFIER_AUTHORITY, _win32_sid_identifier_authority_str, security.sid_identifier_authority, winnt/PSID_IDENTIFIER_AUTHORITY, winnt/SID_IDENTIFIER_AUTHORITY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winnt.h
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
req.typenames: SID_IDENTIFIER_AUTHORITY, *PSID_IDENTIFIER_AUTHORITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	SID_IDENTIFIER_AUTHORITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SID_IDENTIFIER_AUTHORITY structure


## -description


The <b>SID_IDENTIFIER_AUTHORITY</b> structure represents the top-level authority of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID).


## -struct-fields




### -field Value

An array of 6 bytes specifying a SID's top-level authority.


## -remarks



The identifier authority value identifies the agency that issued the SID. The following identifier authorities are predefined.

<table>
<tr>
<th>Identifier authority</th>
<th>Value</th>
</tr>
<tr>
<td>SECURITY_NULL_SID_AUTHORITY</td>
<td>0</td>
</tr>
<tr>
<td>SECURITY_WORLD_SID_AUTHORITY</td>
<td>1</td>
</tr>
<tr>
<td>SECURITY_LOCAL_SID_AUTHORITY</td>
<td>2</td>
</tr>
<tr>
<td>SECURITY_CREATOR_SID_AUTHORITY</td>
<td>3</td>
</tr>
<tr>
<td>SECURITY_NON_UNIQUE_AUTHORITY</td>
<td>4</td>
</tr>
<tr>
<td>SECURITY_NT_AUTHORITY</td>
<td>5</td>
</tr>
<tr>
<td>SECURITY_RESOURCE_MANAGER_AUTHORITY</td>
<td>9</td>
</tr>
</table>
 

A SID must contain a top-level authority and at least one <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">relative identifier</a> (RID) value.




## -see-also




<a href="https://msdn.microsoft.com/fcdff2f8-7f43-4c0f-b548-4914b1991937">AllocateAndInitializeSid</a>



<a href="https://msdn.microsoft.com/67a06e7b-775f-424c-ab36-0fc9b93b801a">GetSidIdentifierAuthority</a>



<a href="https://msdn.microsoft.com/b2d803a5-faaf-4066-ba2c-0442c71bb150">InitializeSid</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>
 

 

