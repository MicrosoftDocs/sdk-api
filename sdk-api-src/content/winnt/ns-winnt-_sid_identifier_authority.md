---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

