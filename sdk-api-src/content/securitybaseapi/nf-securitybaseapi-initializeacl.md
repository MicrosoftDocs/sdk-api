---
UID: NF:securitybaseapi.InitializeAcl
title: InitializeAcl function (securitybaseapi.h)
description: Initializes a new ACL structure.
helpviewer_keywords: ["InitializeAcl","InitializeAcl function [Security]","_win32_initializeacl","security.initializeacl","securitybaseapi/InitializeAcl"]
old-location: security\initializeacl.htm
tech.root: security
ms.assetid: b990a7bd-7840-4c10-baf8-68b3862147f4
ms.date: 12/05/2018
ms.keywords: InitializeAcl, InitializeAcl function [Security], _win32_initializeacl, security.initializeacl, securitybaseapi/InitializeAcl
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitializeAcl
 - securitybaseapi/InitializeAcl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-security-base-l1-2-2.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - InitializeAcl
---

# InitializeAcl function


## -description

The <b>InitializeAcl</b> function initializes a new <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure.

## -parameters

### -param pAcl [out]

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure  to be initialized by this function. Allocate memory for <i>pAcl</i> before calling this function.

### -param nAclLength [in]

The length, in bytes, of the buffer pointed to by the <i>pAcl</i> parameter. This value must be large enough to contain the <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> header and all of the <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs) to be stored in the <b>ACL</b>. In addition, this value must be <b>DWORD</b>-aligned. For more information about calculating the size of an <b>ACL</b>, see Remarks.

### -param dwAclRevision [in]

The revision level of the <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure being created. 


This value can be ACL_REVISION or ACL_REVISION_DS. Use ACL_REVISION_DS if the <a href="/windows/desktop/SecGloss/a-gly">access control list</a> (ACL) supports object-specific ACEs.

## -returns

If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>InitializeAcl</b> function creates an empty <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure; the <b>ACL</b> contains no <a href="/windows/desktop/SecAuthZ/ace">ACEs</a>. Applying an empty <b>ACL</b> to an object denies all access to that object.

The initial size of the <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> depends on the number of <a href="/windows/desktop/SecAuthZ/ace">ACEs</a> you plan to add to the <b>ACL</b> before you use it. For example, if the <b>ACL</b> is to contain an ACE for a user and group, you would initialize the <b>ACL</b> based on two ACEs. For details about modifying an existing <b>ACL</b>, see <a href="/windows/desktop/SecAuthZ/modifying-the-acls-of-an-object-in-c--">Modifying the ACLs of an Object</a>.

To calculate the initial size of an <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>, add the following together, and then align the result to the nearest <b>DWORD</b>:

<ul>
<li>Size of the <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> structure.</li>
<li>Size of each <a href="/windows/desktop/SecAuthZ/ace">ACE</a> structure that the <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> is to contain minus the <b>SidStart</b> member (<b>DWORD</b>) of the ACE.</li>
<li>Length of the SID that each <a href="/windows/desktop/SecAuthZ/ace">ACE</a> is to contain.</li>
</ul>

#### Examples

The following example calls the <b>InitializeAcl</b> function. The size of the  <a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a> is  based on three allow-access <a href="/windows/desktop/SecAuthZ/ace">ACEs</a>. As an option, you can use <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">security descriptor definition language</a> (SDDL) to create the ACL. For details, see <a href="/windows/desktop/SecBP/creating-a-dacl">Creating a DACL</a>.

The example also omits a step for simplification. For more information, see the <a href="/windows/desktop/SecAuthZ/taking-object-ownership-in-c--">Taking Object Ownership</a> example. You must call the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-freesid">FreeSid</a> function at the end of the example code due to calling the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid">AllocateAndInitializeSid</a> function.


```cpp
#include <windows.h>
#include <Winbase.h>
#pragma comment(lib, "duser.lib")

#define NUM_OF_ACES 3

void main()
{
    PACL pAcl = NULL;
    DWORD cbAcl = 0;
    PSID psids[NUM_OF_ACES];

    // Allocate and initialize SIDs.
    // Step omitted - See Taking Object Ownership example.

    // Add the SID for each ACE to psids. 
    cbAcl = sizeof(ACL) + 
        ((sizeof(ACCESS_ALLOWED_ACE)) * NUM_OF_ACES);
    for (int i = 0; i < NUM_OF_ACES; i++)
    {
        cbAcl += GetLengthSid(psids[i]) - sizeof(DWORD);
    }

    // Align cbAcl to a DWORD.
    cbAcl = (cbAcl + (sizeof(DWORD) - 1)) & 0xfffffffc;

    pAcl = (ACL*)LocalAlloc(LPTR, cbAcl);
    if (pAcl)
    {
        if (InitializeAcl(pAcl, cbAcl, ACL_REVISION))
        {

            // Add the ACEs to the ACL.
            // Add the ACL to the object's security descriptor.
        }
        else
        {

            // Handle error.
        }
    }
    {

        // Handle error.
    }

    // Free pAcl when finished.
    // Call FreeSid when finished.
}

```

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-access_allowed_ace">ACCESS_ALLOWED_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-access_denied_ace">ACCESS_DENIED_ACE</a>



<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace">AddAccessAllowedAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace">AddAccessDeniedAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addace">AddAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-addauditaccessace">AddAuditAccessAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-deleteace">DeleteAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getace">GetAce</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getaclinformation">GetAclInformation</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-isvalidacl">IsValidAcl</a>



<a href="/windows/desktop/SecAuthZ/low-level-access-control">Low-level Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Low-level Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setaclinformation">SetAclInformation</a>