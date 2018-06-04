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

# GetEffectiveRightsFromAclW function


## -description


<p class="CCE_Message">[<b>GetEffectiveRightsFromAcl</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the method demonstrated in the example below.]

The <b>GetEffectiveRightsFromAcl</b> function retrieves the effective access rights that an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a> structure grants to a specified trustee. The trustee's effective access rights are the access rights that the <b>ACL</b> grants to the trustee or to any groups of which the trustee is a member.


## -parameters




### -param pacl [in]

A pointer to an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a> structure from which to get the trustee's effective access rights.


### -param pTrustee [in]

A pointer to a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure that identifies the trustee. A trustee can be a user, group, or program (such as a Windows service). You can use a name or a security identifier (<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>) to identify a trustee.


### -param pAccessRights [out]

A pointer to an 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> variable that receives the effective access rights of the trustee.


## -returns




						If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.




## -remarks



The <b>GetEffectiveRightsFromAcl</b> function checks all access-allowed and access-denied <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) in the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL) to determine the effective rights for the trustee. For all ACEs that allow or deny rights to a group, <b>GetEffectiveRightsFromAcl</b> enumerates the members of the group to determine whether the trustee is a member. The function returns an error if it cannot enumerate the members of a group.

A trustee's group rights are enumerated by <b>GetEffectiveRightsFromAcl</b> on the local computer, even if the trustee is accessing objects on a remote computer. This function does not evaluate group rights on remote computers.

The <b>GetEffectiveRightsFromAcl</b>  function does not consider  the following:

<ul>
<li>Implicitly granted access rights, such as READ_CONTROL and WRITE_DAC, for the owner of an object when determining effective rights.</li>
<li>Privileges held by the trustee when determining effective access rights.</li>
<li>Group rights associated with the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>, such as interactive, network, authenticated users, and so forth, in determining effective access rights.</li>
<li><a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">Resource manager</a> policy. For example, for file objects, Delete and Read attributes can be provided by the parent even if they have been denied on the object.</li>
</ul>
The <b>GetEffectiveRightsFromAcl</b> function fails and returns <b>ERROR_INVALID_ACL</b> if the specified ACL contains an inherited access-denied ACE.


#### Examples

The following example shows using <a href="https://msdn.microsoft.com/83df96ff-f3d6-43f8-88b2-6387914b3503">Authz API</a> to get effective access rights from an ACL.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
//  Copyright (C) Microsoft. All rights reserved.

#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;aclapi.h&gt;
#include &lt;tchar.h&gt;
#include &lt;strsafe.h&gt; // for proper buffer handling
#include &lt;authz.h&gt;

#pragma comment(lib, "advapi32.lib")
#pragma comment(lib, "authz.lib")

LPTSTR lpServerName = NULL;


PSID ConvertNameToBinarySid(LPTSTR pAccountName)
{
   LPTSTR pDomainName = NULL;
   DWORD dwDomainNameSize = 0;
   PSID pSid = NULL;
   DWORD dwSidSize = 0;
   SID_NAME_USE sidType;
   BOOL fSuccess = FALSE;
   HRESULT hr = S_OK;

   __try
   {
      LookupAccountName(
            lpServerName,      // look up on local system
            pAccountName,
            pSid,              // buffer to receive name
            &amp;dwSidSize,
            pDomainName,
            &amp;dwDomainNameSize,
            &amp;sidType);
      
      //  If the Name cannot be resolved, LookupAccountName will fail with
      //  ERROR_NONE_MAPPED.
      if (GetLastError() == ERROR_NONE_MAPPED)
      {
         wprintf_s(_T("LookupAccountName failed with %d\n"), GetLastError());
         __leave;
      }
      else if (GetLastError() == ERROR_INSUFFICIENT_BUFFER)
      {
         pSid = (LPTSTR)LocalAlloc(LPTR, dwSidSize * sizeof(TCHAR));
         if (pSid == NULL)
         {
            wprintf_s(_T("LocalAlloc failed with %d\n"), GetLastError());
            __leave;
         }

         pDomainName = (LPTSTR)LocalAlloc(LPTR, dwDomainNameSize * sizeof(TCHAR));
         if (pDomainName == NULL)
         {
            wprintf_s(_T("LocalAlloc failed with %d\n"), GetLastError());
            __leave;
         }

         if (!LookupAccountName(
               lpServerName,      // look up on local system
               pAccountName,
               pSid,              // buffer to receive name
               &amp;dwSidSize,
               pDomainName,
               &amp;dwDomainNameSize,
               &amp;sidType))
         {
            wprintf_s(_T("LookupAccountName failed with %d\n"), GetLastError());
            __leave;
         }
      }
      
      //  Any other error code
      else
      {
         wprintf_s(_T("LookupAccountName failed with %d\n"), GetLastError());
         __leave;
      }

      fSuccess = TRUE;
   }
   __finally
   {
      if(pDomainName != NULL)
      {
          LocalFree(pDomainName);
          pDomainName = NULL;
      }
      
      //  Free pSid only if failed;
      //  otherwise, the caller has to free it after use.
      if (fSuccess == FALSE)
      {
         if(pSid != NULL)
      {
          LocalFree(pSid);
          pSid = NULL;
      }
      }
   }

   return pSid;
}


void DisplayError(char* pszAPI, DWORD dwError)
{
   LPVOID lpvMessageBuffer;

   if (!FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_HMODULE | FORMAT_MESSAGE_FROM_SYSTEM,
              GetModuleHandle(L"Kernel32.dll"), dwError, 
              MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),  // the user default language
              (LPTSTR)&amp;lpvMessageBuffer, 0, NULL))
   {
      wprintf_s(L"FormatMessage failed with %d\n", GetLastError());
      ExitProcess(GetLastError());
   }

   //  ...now display this string.
   wprintf_s(L"ERROR: API        = %s.\n", (char *)pszAPI);
   wprintf_s(L"       error code = %08X.\n", dwError);
   wprintf_s(L"       message    = %s.\n", (char *)lpvMessageBuffer);

   //  Free the buffer allocated by the system.
   LocalFree(lpvMessageBuffer);

   ExitProcess(GetLastError());
}

void DisplayAccessMask(ACCESS_MASK Mask)
{
      // This evaluation of the ACCESS_MASK is an example. 
      // Applications should evaluate the ACCESS_MASK as necessary.

   wprintf_s(L"Effective Allowed Access Mask : %8X\n", Mask);
   if (((Mask &amp; GENERIC_ALL) == GENERIC_ALL)
      || ((Mask &amp; FILE_ALL_ACCESS) == FILE_ALL_ACCESS))
   {
         wprintf_s(L"Full Control\n");
         return;
   }
   if (((Mask &amp; GENERIC_READ) == GENERIC_READ)
      || ((Mask &amp; FILE_GENERIC_READ) == FILE_GENERIC_READ))
         wprintf_s(L"Read\n");
   if (((Mask &amp; GENERIC_WRITE) == GENERIC_WRITE)
      || ((Mask &amp; FILE_GENERIC_WRITE) == FILE_GENERIC_WRITE))
         wprintf_s(L"Write\n");
   if (((Mask &amp; GENERIC_EXECUTE) == GENERIC_EXECUTE)
      || ((Mask &amp; FILE_GENERIC_EXECUTE) == FILE_GENERIC_EXECUTE))
         wprintf_s(L"Execute\n");

}

void GetAccess(AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClient, PSECURITY_DESCRIPTOR psd)
{
   AUTHZ_ACCESS_REQUEST AccessRequest = {0};
   AUTHZ_ACCESS_REPLY AccessReply = {0};
   BYTE     Buffer[1024];
   BOOL bRes = FALSE;  // assume error

   //  Do AccessCheck.
   AccessRequest.DesiredAccess = MAXIMUM_ALLOWED;
   AccessRequest.PrincipalSelfSid = NULL;
   AccessRequest.ObjectTypeList = NULL;
   AccessRequest.ObjectTypeListLength = 0;
   AccessRequest.OptionalArguments = NULL; 

   RtlZeroMemory(Buffer, sizeof(Buffer));
   AccessReply.ResultListLength = 1;
   AccessReply.GrantedAccessMask = (PACCESS_MASK) (Buffer);
   AccessReply.Error = (PDWORD) (Buffer + sizeof(ACCESS_MASK));


   if (!AuthzAccessCheck( 0,
                          hAuthzClient,
                          &amp;AccessRequest,
                          NULL,
                          psd,
                          NULL,
                          0,
                          &amp;AccessReply,
                          NULL) ) {
      wprintf_s(_T("AuthzAccessCheck failed with %d\n"), GetLastError());
   }
   else 
      DisplayAccessMask(*(PACCESS_MASK)(AccessReply.GrantedAccessMask));

   return;
}

BOOL GetEffectiveRightsForUser(AUTHZ_RESOURCE_MANAGER_HANDLE hManager,
                               PSECURITY_DESCRIPTOR psd,
                                      LPTSTR lpszUserName)
{
   PSID pSid = NULL;
   BOOL bResult = FALSE;
   LUID unusedId = { 0 };
   AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext = NULL;

   pSid = ConvertNameToBinarySid(lpszUserName);
   if (pSid != NULL)
   {
      bResult = AuthzInitializeContextFromSid(0,
         pSid,
         hManager,
         NULL,
         unusedId,
         NULL,
         &amp;hAuthzClientContext);
      if (bResult)
      {
         GetAccess(hAuthzClientContext, psd);
         AuthzFreeContext(hAuthzClientContext);
      }
      else
         wprintf_s(_T("AuthzInitializeContextFromSid failed with %d\n"), GetLastError());
   }
    if(pSid != NULL)
      {
          LocalFree(pSid);
          pSid = NULL;
      }

   return bResult;
}

void UseAuthzSolution(PSECURITY_DESCRIPTOR psd, LPTSTR lpszUserName)
{
   AUTHZ_RESOURCE_MANAGER_HANDLE hManager;
   BOOL bResult = FALSE;

   bResult = AuthzInitializeResourceManager(AUTHZ_RM_FLAG_NO_AUDIT,
      NULL, NULL, NULL, NULL, &amp;hManager);
   if (bResult)
   {
      bResult = GetEffectiveRightsForUser(hManager, psd, lpszUserName);
      AuthzFreeResourceManager(hManager);
   }
   else
      wprintf_s(_T("AuthzInitializeResourceManager failed with %d\n"), GetLastError());
}


void wmain(int argc, wchar_t *argv[])
{
   DWORD                dw;
   PACL                 pacl;
   PSECURITY_DESCRIPTOR psd;
   PSID                 psid = NULL; 

   if (argc != 3)
   {
      wprintf_s(L"Usage: FileOrFolderName UserOrGroupName\n");
      wprintf_s(L"Usage: FileOrFolderName UserOrGroupName\n");
      return;
   }
  

    dw = GetNamedSecurityInfo(argv[1], SE_FILE_OBJECT, DACL_SECURITY_INFORMATION | 
      OWNER_SECURITY_INFORMATION |
      GROUP_SECURITY_INFORMATION, NULL, NULL, &amp;pacl, NULL, &amp;psd);
   if (dw != ERROR_SUCCESS)
   {  printf("couldn't do getnamedsecinfo \n");
      DisplayError("GetNamedSecurityInfo", dw);
   }

   
   UseAuthzSolution(psd, argv[2]);


   if(psid != NULL)
      {
          LocalFree(psid);
          psid = NULL;
      };

   LocalFree(psd);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538796">ACCESS_ALLOWED_ACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538831">ACCESS_DENIED_ACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538844">ACE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a>



<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control Overview</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/4381fe12-5fb3-4f9c-8daa-261cb1a466ec">GetAuditedPermissionsFromAcl</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 

