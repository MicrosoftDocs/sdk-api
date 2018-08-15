---
UID: NF:userenv.FreeGPOListW
title: FreeGPOListW function
author: windows-sdk-content
description: The FreeGPOList function frees the specified list of GPOs.
old-location: policy\freegpolist.htm
old-project: Policy
ms.assetid: 96bd2b5b-c088-4eea-bbc2-31d83c13aa99
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FreeGPOList, FreeGPOList function [Group Policy], FreeGPOListA, FreeGPOListW, _win32_freegpolist, policy.freegpolist, userenv/FreeGPOList, userenv/FreeGPOListA, userenv/FreeGPOListW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: userenv.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: USB_UNICODE_NAME, *PUSB_UNICODE_NAME
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
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
req.product: Windows UI
---

# FreeGPOListW function


## -description


The
    <b>FreeGPOList</b> function frees the specified list of GPOs.


## -parameters




### -param pGPOList [in]

A pointer to the list of GPO structures. This list is returned by the 
<a href="https://msdn.microsoft.com/26c54ac5-23d7-40ed-94a9-70d25e14431f">GetGPOList</a> or 
<a href="https://msdn.microsoft.com/11e80a4e-acc4-4229-aa34-8f7d083c1041">GetAppliedGPOList</a> function. For more information, see 
<a href="https://msdn.microsoft.com/7275a3cd-6b19-4eb9-9481-b73bd5af5753">GROUP_POLICY_OBJECT</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/7275a3cd-6b19-4eb9-9481-b73bd5af5753">GROUP_POLICY_OBJECT</a>



<a href="https://msdn.microsoft.com/11e80a4e-acc4-4229-aa34-8f7d083c1041">GetAppliedGPOList</a>



<a href="https://msdn.microsoft.com/26c54ac5-23d7-40ed-94a9-70d25e14431f">GetGPOList</a>



<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>
 

 

