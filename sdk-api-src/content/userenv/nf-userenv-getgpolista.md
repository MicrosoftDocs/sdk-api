---
UID: NF:userenv.GetGPOListA
title: GetGPOListA function (userenv.h)
description: The GetGPOList function retrieves the list of GPOs for the specified user or computer. (ANSI)
helpviewer_keywords: ["GetGPOListA", "userenv/GetGPOListA"]
old-location: policy\getgpolist.htm
tech.root: Policy
ms.assetid: 26c54ac5-23d7-40ed-94a9-70d25e14431f
ms.date: 12/05/2018
ms.keywords: GetGPOList, GetGPOList function [Group Policy], GetGPOListA, GetGPOListW, _win32_getgpolist, policy.getgpolist, userenv/GetGPOList, userenv/GetGPOListA, userenv/GetGPOListW
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
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetGPOListA
 - userenv/GetGPOListA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - GetGPOList
 - GetGPOListA
 - GetGPOListW
---

# GetGPOListA function


## -description

The
    <b>GetGPOList</b> function retrieves the list of GPOs for the specified user or computer. This function can be called in two ways: first, you can use the token for the user or computer, or, second, you can use the name of the user or computer and the name of the domain controller.

## -parameters

### -param hToken [in]

A token for the user or computer, returned from the 
<a href="/windows/desktop/api/winbase/nf-winbase-logonusera">LogonUser</a>, 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken">CreateRestrictedToken</a>, 
<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-duplicatetoken">DuplicateToken</a>, 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken">OpenProcessToken</a>, or 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken">OpenThreadToken</a> function. This token must have <b>TOKEN_IMPERSONATE</b> and <b>TOKEN_QUERY</b> access. For more information, see 
<a href="/windows/desktop/SecAuthZ/access-rights-for-access-token-objects">Access Rights for Access-Token Objects</a> and the following Remarks section.

If this parameter is <b>NULL</b>, you must supply values for the <i>lpName</i> and <i>lpHostName</i> parameters.

### -param lpName [in]

A pointer to the user or computer name, in the fully qualified distinguished name format (for example,  "CN=<i>user</i>, OU=<i>users</i>, DC=<i>contoso</i>, DC=<i>com</i>").

If the <i>hToken</i> parameter is not <b>NULL</b>, this parameter must be <b>NULL</b>.

### -param lpHostName [in]

A DNS domain name (preferred) or domain controller name. Domain controller name can be retrieved using the 
<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function, specifying <b>DS_DIRECTORY_SERVICE_REQUIRED</b> in the <i>flags</i> parameter.

If the <i>hToken</i> parameter is not <b>NULL</b>, this parameter must be <b>NULL</b>.

### -param lpComputerName [in]

A pointer to the name of the computer used to determine the site location. The format of the name is "&#92;&#92;<i>computer_name</i>". If this parameter is <b>NULL</b>, the local computer name is used.

### -param dwFlags [in]

A value that specifies additional flags that are used to control information retrieval. If you specify <b>GPO_LIST_FLAG_MACHINE</b>, the function retrieves policy information for the computer. If you do not specify <b>GPO_LIST_FLAG_MACHINE</b>, the function retrieves policy information for the user.

If you specify <b>GPO_LIST_FLAG_SITEONLY</b> the function returns only site information for the computer or user.

### -param pGPOList [out]

A pointer that receives the list of GPO structures. For more information, see 
<a href="/windows/desktop/api/userenv/ns-userenv-group_policy_objecta">GROUP_POLICY_OBJECT</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>GetGPOList</b> function is intended for use by services acting on behalf of a user or computer. The service calls this function to obtain a list of GPOs, then checks each GPO for service-specific policy.

Calling this function with a token provides the most accurate list. The system can perform access checking for the user or computer. Calling this function with the user or computer name and the domain controller name is faster than calling it with a token. However, if the token is not specified, the system uses the security access of the caller, which means that the list may not be completely correct for the intended user or computer.

To obtain the most accurate list of GPOs for a computer when calling <b>GetGPOList</b>, the caller must have read access to each OU and site in the computer domain, and also read and apply Group Policy access to all GPOs that are linked to the sites, domain or OUs of that domain. An example of a caller would be a service running on the computer whose name is specified in the <i>lpName</i> parameter. An alternate method of obtaining a list of GPOs would be to call the <a href="/previous-versions/windows/desktop/Policy/rsopplanningmodeprovider-rsopcreatesession">RsopCreateSession</a> method of the <b>RsopPlanningModeProvider</b> WMI class. The method can generate resultant policy data for a computer or user account in a hypothetical scenario.

Call the 
<a href="/windows/desktop/api/userenv/nf-userenv-freegpolista">FreeGPOList</a> function to free the GPO list when you have finished processing it.

Generally, you should call 
<b>GetGPOList</b> with a token when retrieving a list of GPOs for a user as shown in the following code example.


```cpp
LPGROUP_POLICY_OBJECT  pGPOList;
      if (GetGPOList (hToken, NULL, NULL, NULL, 0, &pGPOList))
      {
//        Perform processing here. 
//
//        Free the GPO list when you finish processing.
          FreeGPOList (pGPOList);
      }
```


Typically, to retrieve a list of GPOs for a computer, you can call 
<b>GetGPOList</b> with the computer name and domain controller name as demonstrated in the following code snippet.


```cpp
LPGROUP_POLICY_OBJECT  pGPOList;
      if (GetGPOList (NULL, lpMachineName, lpHostName, lpMachineName, GPO_LIST_FLAG_MACHINE, &pGPOList))
      {
//        Perform processing here. 
//
//        Free the GPO list when you finish processing.
          FreeGPOList (pGPOList);
      }
```


To retrieve the list of GPOs applied for a specific user or computer and extension, call the 
<a href="/windows/desktop/api/userenv/nf-userenv-getappliedgpolista">GetAppliedGPOList</a> function.





> [!NOTE]
> The userenv.h header defines GetGPOList as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>



<a href="/windows/desktop/api/userenv/nf-userenv-freegpolista">FreeGPOList</a>



<a href="/windows/desktop/api/userenv/ns-userenv-group_policy_objecta">GROUP_POLICY_OBJECT</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>
