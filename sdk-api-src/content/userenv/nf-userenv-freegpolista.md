---
UID: NF:userenv.FreeGPOListA
title: FreeGPOListA function (userenv.h)
author: windows-sdk-content
description: The FreeGPOList function frees the specified list of GPOs.
old-location: policy\freegpolist.htm
tech.root: Policy
ms.assetid: 96bd2b5b-c088-4eea-bbc2-31d83c13aa99
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FreeGPOList, FreeGPOList function [Group Policy], FreeGPOListA, FreeGPOListW, _win32_freegpolist, policy.freegpolist, userenv/FreeGPOList, userenv/FreeGPOListA, userenv/FreeGPOListW
ms.topic: function
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FreeGPOListW (Unicode) and FreeGPOListA (ANSI)
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
 - FreeGPOList
 - FreeGPOListA
 - FreeGPOListW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FreeGPOListA function


## -description


The
    <b>FreeGPOList</b> function frees the specified list of GPOs.


## -parameters




### -param pGPOList [in]

A pointer to the list of GPO structures. This list is returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-getgpolista">GetGPOList</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-getappliedgpolista">GetAppliedGPOList</a> function. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/api/userenv/ns-userenv-_group_policy_objecta">GROUP_POLICY_OBJECT</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/userenv/ns-userenv-_group_policy_objecta">GROUP_POLICY_OBJECT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-getappliedgpolista">GetAppliedGPOList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/userenv/nf-userenv-getgpolista">GetGPOList</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>
 

 

