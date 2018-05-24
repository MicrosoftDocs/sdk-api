---
UID: NF:userenv.GetGPOListW
title: GetGPOListW function
author: windows-driver-content
description: The GetGPOList function retrieves the list of GPOs for the specified user or computer.
old-location: policy\getgpolist.htm
old-project: Policy
ms.assetid: 26c54ac5-23d7-40ed-94a9-70d25e14431f
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: GetGPOList, GetGPOList function [Group Policy], GetGPOListA, GetGPOListW, _win32_getgpolist, policy.getgpolist, userenv/GetGPOList, userenv/GetGPOListA, userenv/GetGPOListW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetGPOListW (Unicode) and GetGPOListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Userenv.dll
api_name:
-	GetGPOList
-	GetGPOListA
-	GetGPOListW
product: Windows
targetos: Windows
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# GetGPOListW function


## -description


The
    <b>GetGPOList</b> function retrieves the list of GPOs for the specified user or computer. This function can be called in two ways: first, you can use the token for the user or computer, or, second, you can use the name of the user or computer and the name of the domain controller.


## -parameters




### -param hToken [in]

A token for the user or computer, returned from the 
<a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a>, 
<a href="https://msdn.microsoft.com/e087f360-5d1d-4846-b3d6-214a426e5222">CreateRestrictedToken</a>, 
<a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a>, 
<a href="https://msdn.microsoft.com/1e760ad8-7e46-4748-8c45-36ad8efe936a">OpenProcessToken</a>, or 
<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a> function. This token must have <b>TOKEN_IMPERSONATE</b> and <b>TOKEN_QUERY</b> access. For more information, see 
<a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a> and the following Remarks section.

If this parameter is <b>NULL</b>, you must supply values for the <i>lpName</i> and <i>lpHostName</i> parameters.


### -param lpName [in]

A pointer to the user or computer name, in the fully qualified distinguished name format (for example,  "CN=<i>user</i>, OU=<i>users</i>, DC=<i>contoso</i>, DC=<i>com</i>").

If the <i>hToken</i> parameter is not <b>NULL</b>, this parameter must be <b>NULL</b>.


### -param lpHostName [in]

A DNS domain name or domain controller name. Domain controller name can be retrieved using the 
<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a> function, specifying <b>DS_DIRECTORY_SERVICE_REQUIRED</b> in the <i>flags</i> parameter.

If the <i>hToken</i> parameter is not <b>NULL</b>, this parameter must be <b>NULL</b>.


### -param lpComputerName [in]

A pointer to the name of the computer used to determine the site location. The format of the name is "\\<i>computer_name</i>". If this parameter is <b>NULL</b>, the local computer name is used.


### -param dwFlags [in]

A value that specifies additional flags that are used to control information retrieval. If you specify <b>GPO_LIST_FLAG_MACHINE</b>, the function retrieves policy information for the computer. If you do not specify <b>GPO_LIST_FLAG_MACHINE</b>, the function retrieves policy information for the user.

If you specify <b>GPO_LIST_FLAG_SITEONLY</b> the function returns only site information for the computer or user.


### -param pGPOList [out]

A pointer that receives the list of GPO structures. For more information, see 
<a href="https://msdn.microsoft.com/7275a3cd-6b19-4eb9-9481-b73bd5af5753">GROUP_POLICY_OBJECT</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>GetGPOList</b> function is intended for use by services acting on behalf of a user or computer. The service calls this function to obtain a list of GPOs, then checks each GPO for service-specific policy.

Calling this function with a token provides the most accurate list. The system can perform access checking for the user or computer. Calling this function with the user or computer name and the domain controller name is faster than calling it with a token. However, if the token is not specified, the system uses the security access of the caller, which means that the list may not be completely correct for the intended user or computer.

To obtain the most accurate list of GPOs for a computer when calling <b>GetGPOList</b>, the caller must have read access to each OU and site in the computer domain, and also read and apply Group Policy access to all GPOs that are linked to the sites, domain or OUs of that domain. An example of a caller would be a service running on the computer whose name is specified in the <i>lpName</i> parameter. An alternate method of obtaining a list of GPOs would be to call the <a href="https://msdn.microsoft.com/b1ae83e4-ce48-4c4d-af95-eab3d1221188">RsopCreateSession</a> method of the <b>RsopPlanningModeProvider</b> WMI class. The method can generate resultant policy data for a computer or user account in a hypothetical scenario.

Call the 
<a href="https://msdn.microsoft.com/96bd2b5b-c088-4eea-bbc2-31d83c13aa99">FreeGPOList</a> function to free the GPO list when you have finished processing it.

Generally, you should call 
<b>GetGPOList</b> with a token when retrieving a list of GPOs for a user as shown in the following code example.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LPGROUP_POLICY_OBJECT  pGPOList;
      if (GetGPOList (hToken, NULL, NULL, NULL, 0, &amp;pGPOList))
      {
//        Perform processing here. 
//
//        Free the GPO list when you finish processing.
          FreeGPOList (pGPOList);
      }</pre>
</td>
</tr>
</table></span></div>
Typically, to retrieve a list of GPOs for a computer, you can call 
<b>GetGPOList</b> with the computer name and domain controller name as demonstrated in the following code snippet.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LPGROUP_POLICY_OBJECT  pGPOList;
      if (GetGPOList (NULL, lpMachineName, lpHostName, lpMachineName, GPO_LIST_FLAG_MACHINE, &amp;pGPOList))
      {
//        Perform processing here. 
//
//        Free the GPO list when you finish processing.
          FreeGPOList (pGPOList);
      }</pre>
</td>
</tr>
</table></span></div>
To retrieve the list of GPOs applied for a specific user or computer and extension, call the 
<a href="https://msdn.microsoft.com/11e80a4e-acc4-4229-aa34-8f7d083c1041">GetAppliedGPOList</a> function.




## -see-also




<a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a>



<a href="https://msdn.microsoft.com/96bd2b5b-c088-4eea-bbc2-31d83c13aa99">FreeGPOList</a>



<a href="https://msdn.microsoft.com/7275a3cd-6b19-4eb9-9481-b73bd5af5753">GROUP_POLICY_OBJECT</a>



<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>
 

 

