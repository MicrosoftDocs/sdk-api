---
UID: NF:cfgmgr32.CM_Free_Res_Des_Handle
title: CM_Free_Res_Des_Handle function
author: windows-sdk-content
description: The CM_Free_Res_Des_Handle function invalidates a resource description handle and frees its associated memory allocation.
old-location: devinst\cm_free_res_des_handle.htm
tech.root: devinst
ms.assetid: 4a585d64-fd00-47a8-8ada-7e343beb829d
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CM_Free_Res_Des_Handle, CM_Free_Res_Des_Handle function [Device and Driver Installation], cfgmgr32/CM_Free_Res_Des_Handle, cfgmgrfn_a3dd0de4-8188-4117-9e8b-ecc5eb448096.xml, devinst.cm_free_res_des_handle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cfgmgr32.dll
api_name:
 - CM_Free_Res_Des_Handle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Free_Res_Des_Handle function


## -description


The <b>CM_Free_Res_Des_Handle</b> function invalidates a resource description handle and frees its associated memory allocation.


## -parameters




### -param rdResDes [in]

Caller-supplied resource descriptor handle to be freed. This handle must have been previously obtained by calling one of the following functions:


<a href="https://msdn.microsoft.com/0097b53a-c1c8-4e76-beef-812a953073b6">CM_Add_Res_Des</a>



<a href="https://msdn.microsoft.com/f19996ae-f243-4e8c-b200-7d11c06490c9">CM_Add_Res_Des_Ex</a>



<a href="https://msdn.microsoft.com/2ce2a84c-a9fe-42ff-920f-47dd0f54a820">CM_Get_Next_Res_Des</a>



<a href="https://msdn.microsoft.com/91e9a686-2465-4ae8-9cc2-391cd98c2138">CM_Get_Next_Res_Des_Ex</a>



<a href="https://msdn.microsoft.com/9320c396-4da8-4b35-a620-4bb7cbd80e9a">CM_Modify_Res_Des</a>



<a href="https://msdn.microsoft.com/6bb4af46-995e-4487-9c5f-89c72abb0ec5">CM_Modify_Res_Des_Ex</a>



## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



Each time your code calls one of the functions listed under the description of <i>rdResDes</i>, it must subsequently call <b>CM_Free_Res_Des_Handle</b>.



