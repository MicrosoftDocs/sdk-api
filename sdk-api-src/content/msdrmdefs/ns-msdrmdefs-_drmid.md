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

# _DRMID structure


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMID</b> structure identifies an object. It is used by the <a href="https://msdn.microsoft.com/25820f49-ffa8-40c4-87fc-ce4909ec20ed">DRMBOUNDLICENSEPARAMS</a> structure and by the <a href="https://msdn.microsoft.com/92858a46-cef5-4d25-9f3c-cbb343743565">DRMCreateEnablingPrincipal</a> function.


## -struct-fields




### -field uVersion

Specifies the version of the structure. If you are programming in C, this should be set to <b>DRMIDVERSION</b> (0).


### -field wszIDType

A pointer to a null-terminated Unicode string that contains the ID type. If you are using this parameter to create a bound license, you must specify the same value that you set in the <i>wszIDType</i> parameter of the <a href="https://msdn.microsoft.com/dcf95e9e-e2de-449e-a45a-4974094ecb7e">DRMSetMetaData</a> function. For more information, see <a href="https://msdn.microsoft.com/25820f49-ffa8-40c4-87fc-ce4909ec20ed">DRMBOUNDLICENSEPARAMS</a>. If you are using this parameter in  the <a href="https://msdn.microsoft.com/92858a46-cef5-4d25-9f3c-cbb343743565">DRMCreateEnablingPrincipal</a> function, the value can be <b>NULL</b>.


### -field wszID

A pointer to a null-terminated Unicode string that contains the object ID. If you are using this parameter to create a bound license, you must specify the same value that you set in the <i>wszID</i> parameter of the <a href="https://msdn.microsoft.com/dcf95e9e-e2de-449e-a45a-4974094ecb7e">DRMSetMetaData</a> function. For more information, see <a href="https://msdn.microsoft.com/25820f49-ffa8-40c4-87fc-ce4909ec20ed">DRMBOUNDLICENSEPARAMS</a>. If you are using this parameter in  the <a href="https://msdn.microsoft.com/92858a46-cef5-4d25-9f3c-cbb343743565">DRMCreateEnablingPrincipal</a> function, the value can be <b>NULL</b>.


## -remarks



In a C++ application, this structure will have a default constructor that initializes the members to the following values.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>uVersion = DRMIDVERSION
wszIDType = NULL
wszID = NULL
</pre>
</td>
</tr>
</table></span></div>
An overloaded C++ constructor is also defined as follows.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DRMID(PWSTR wszIDType, PWSTR wszID)</pre>
</td>
</tr>
</table></span></div>
 This constructor will initialize the members to the following values.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>uVersion = DRMIDVERSION
wszIDType = wszTypein
wszID = wszIDin
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/06a0c6d2-108d-4c72-9ae6-8959304602c5">AD RMS Structures</a>



<a href="https://msdn.microsoft.com/25820f49-ffa8-40c4-87fc-ce4909ec20ed">DRMBOUNDLICENSEPARAMS</a>
 

 

