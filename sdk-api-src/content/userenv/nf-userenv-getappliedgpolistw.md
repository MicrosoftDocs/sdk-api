---
UID: NF:userenv.GetAppliedGPOListW
title: GetAppliedGPOListW function
author: windows-sdk-content
description: The GetAppliedGPOList function retrieves the list of GPOs applied for the specified user or computer.
old-location: policy\getappliedgpolist.htm
tech.root: Policy
ms.assetid: 11e80a4e-acc4-4229-aa34-8f7d083c1041
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPO_LIST_FLAG_MACHINE, GetAppliedGPOList, GetAppliedGPOList function [Group Policy], GetAppliedGPOListA, GetAppliedGPOListW, _win32_getappliedgpolist, policy.getappliedgpolist, userenv/GetAppliedGPOList, userenv/GetAppliedGPOListA, userenv/GetAppliedGPOListW
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
req.unicode-ansi: GetAppliedGPOListW (Unicode) and GetAppliedGPOListA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - GetAppliedGPOList
 - GetAppliedGPOListA
 - GetAppliedGPOListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetAppliedGPOListW function


## -description


The
    <b>GetAppliedGPOList</b> function retrieves the list of GPOs applied for the specified user or computer.


## -parameters




### -param dwFlags [in]

A value that specifies the policy type. This parameter can be the following value.



#### GPO_LIST_FLAG_MACHINE

Retrieves information  about the computer policy.

If this value is not specified, the function retrieves only user policy information.


### -param pMachineName [in]

A pointer to the name of the remote computer. The format of the name is "\\<i>computer_name</i>". If this parameter is <b>NULL</b>, the local computer name is used.


### -param pSidUser [in]

A value that specifies the SID of the user. If <i>pMachineName</i> is not <b>NULL</b> and <i>dwFlags</i> specifies user policy, then <i>pSidUser</i> cannot be <b>NULL</b>.

If <i>pMachineName</i> is <b>NULL</b> and <i>pSidUser</i> is <b>NULL</b>, the user is the currently logged-on user. If <i>pMachineName</i> is <b>NULL</b> and <i>pSidUser</i> is not <b>NULL</b>, the user is represented by <i>pSidUser</i> on the local computer. For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa379571(v=VS.85).aspx">Security Identifiers</a>.


### -param pGuidExtension [in]

A value that specifies the <b>GUID</b> of the extension.


### -param ppGPOList [out]

A pointer that receives the list of GPO structures. For more information, see 
<a href="https://msdn.microsoft.com/7275a3cd-6b19-4eb9-9481-b73bd5af5753">GROUP_POLICY_OBJECT</a>.


##### - dwFlags.GPO_LIST_FLAG_MACHINE

Retrieves information  about the computer policy.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function returns a system error code. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a> or the header file WinError.h.




## -remarks



To free the GPO list when you have finished processing it, call the 
<a href="https://msdn.microsoft.com/96bd2b5b-c088-4eea-bbc2-31d83c13aa99">FreeGPOList</a> function.




## -see-also




<a href="https://msdn.microsoft.com/96bd2b5b-c088-4eea-bbc2-31d83c13aa99">FreeGPOList</a>



<a href="https://msdn.microsoft.com/7275a3cd-6b19-4eb9-9481-b73bd5af5753">GROUP_POLICY_OBJECT</a>



<a href="https://msdn.microsoft.com/26c54ac5-23d7-40ed-94a9-70d25e14431f">GetGPOList</a>



<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>
 

 

