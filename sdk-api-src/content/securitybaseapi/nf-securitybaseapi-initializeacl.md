---
UID: NF:securitybaseapi.InitializeAcl
title: InitializeAcl function
author: windows-sdk-content
description: Initializes a new ACL structure.
old-location: security\initializeacl.htm
tech.root: secauthz
ms.assetid: b990a7bd-7840-4c10-baf8-68b3862147f4
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: InitializeAcl, InitializeAcl function [Security], _win32_initializeacl, security.initializeacl, securitybaseapi/InitializeAcl
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
 - InitializeAcl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InitializeAcl function


## -description


The <b>InitializeAcl</b> function initializes a new <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure.


## -parameters




### -param pAcl [out]

A pointer to an 
<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure  to be initialized by this function. Allocate memory for <i>pAcl</i> before calling this function.


### -param nAclLength [in]

The length, in bytes, of the buffer pointed to by the <i>pAcl</i> parameter. This value must be large enough to contain the <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> header and all of the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) to be stored in the <b>ACL</b>. In addition, this value must be <b>DWORD</b>-aligned. For more information about calculating the size of an <b>ACL</b>, see Remarks.


### -param dwAclRevision [in]

The revision level of the <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure being created. 


This value can be ACL_REVISION or ACL_REVISION_DS. Use ACL_REVISION_DS if the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL) supports object-specific ACEs.


## -returns



If the function succeeds, the function returns nonzero.
      

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>InitializeAcl</b> function creates an empty <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure; the <b>ACL</b> contains no <a href="https://msdn.microsoft.com/980b8242-2ba2-469f-b834-da7d3fb22e14">ACEs</a>. Applying an empty <b>ACL</b> to an object denies all access to that object.

The initial size of the <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> depends on the number of <a href="https://msdn.microsoft.com/980b8242-2ba2-469f-b834-da7d3fb22e14">ACEs</a> you plan to add to the <b>ACL</b> before you use it. For example, if the <b>ACL</b> is to contain an ACE for a user and group, you would initialize the <b>ACL</b> based on two ACEs. For details about modifying an existing <b>ACL</b>, see <a href="https://msdn.microsoft.com/0c168bb7-996f-42a8-96cd-2ba7870a3333">Modifying the ACLs of an Object</a>.

To calculate the initial size of an <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>, add the following together, and then align the result to the nearest <b>DWORD</b>:

<ul>
<li>Size of the <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> structure.</li>
<li>Size of each <a href="https://msdn.microsoft.com/980b8242-2ba2-469f-b834-da7d3fb22e14">ACE</a> structure that the <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> is to contain minus the <b>SidStart</b> member (<b>DWORD</b>) of the ACE.</li>
<li>Length of the SID that each <a href="https://msdn.microsoft.com/980b8242-2ba2-469f-b834-da7d3fb22e14">ACE</a> is to contain.</li>
</ul>

#### Examples

The following example calls the <b>InitializeAcl</b> function. The size of the  <a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a> is  based on three allow-access <a href="https://msdn.microsoft.com/980b8242-2ba2-469f-b834-da7d3fb22e14">ACEs</a>. As an option, you can use <a href="https://msdn.microsoft.com/2b15325e-34ed-497b-ae6d-3ec3ac168232">security descriptor definition language</a> (SDDL) to create the ACL. For details, see <a href="https://msdn.microsoft.com/f8ec202f-4f34-4123-8f3c-cfc5960b4dc2">Creating a DACL</a>.

The example also omits a step for simplification. For more information, see the <a href="https://msdn.microsoft.com/0b309ac9-177d-425f-8b78-71fe73e41979">Taking Object Ownership</a> example. You must call the <a href="https://msdn.microsoft.com/1e2098d8-4d1f-4353-97c1-549021a5b3fd">FreeSid</a> function at the end of the example code due to calling the <a href="https://msdn.microsoft.com/fcdff2f8-7f43-4c0f-b548-4914b1991937">AllocateAndInitializeSid</a> function.


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




<a href="https://msdn.microsoft.com/002a3fa7-02a3-4832-948e-b048f5f5818f">ACCESS_ALLOWED_ACE</a>



<a href="https://msdn.microsoft.com/d76a92d0-ccd0-4e73-98b6-43bcd661134d">ACCESS_DENIED_ACE</a>



<a href="https://msdn.microsoft.com/0073659f-c4d5-4aaf-aaa6-ea596d3bd8b9">ACL</a>



<a href="https://msdn.microsoft.com/1004353a-f907-4452-9c0f-85eba0ece813">AddAccessAllowedAce</a>



<a href="https://msdn.microsoft.com/5b4c4164-48f4-4cd5-b60e-554f2498d547">AddAccessDeniedAce</a>



<a href="https://msdn.microsoft.com/f472d864-a273-49b5-b5e2-98772989971e">AddAce</a>



<a href="https://msdn.microsoft.com/34f22aea-9cde-411e-b2d5-bfcd3bfe325d">AddAuditAccessAce</a>



<a href="https://msdn.microsoft.com/02ce45ad-3d51-4548-848e-a62bf4bf72a8">DeleteAce</a>



<a href="https://msdn.microsoft.com/5b5d8751-20d7-40a2-bd70-cfbe956aaa03">GetAce</a>



<a href="https://msdn.microsoft.com/23ef6abd-03e9-439e-ba05-629c8d61cd66">GetAclInformation</a>



<a href="https://msdn.microsoft.com/3ae9f147-4e90-44df-a1af-cf6ebad92aea">IsValidAcl</a>



<a href="https://msdn.microsoft.com/16337b77-23c5-4b7a-a344-66a02ee0e8a8">Low-level Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Low-level Access Control Functions</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/bb4dd7f9-2f15-4a27-89c9-1675f4fb8d92">SetAclInformation</a>
 

 

