---
UID: NF:cfgmgr32.CM_Free_Res_Des_Handle
title: CM_Free_Res_Des_Handle function
author: windows-sdk-content
description: The CM_Free_Res_Des_Handle function invalidates a resource description handle and frees its associated memory allocation.
old-location: devinst\cm_free_res_des_handle.htm
old-project: devinst
ms.assetid: 4a585d64-fd00-47a8-8ada-7e343beb829d
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: CM_Free_Res_Des_Handle, CM_Free_Res_Des_Handle function [Device and Driver Installation], cfgmgr32/CM_Free_Res_Des_Handle, cfgmgrfn_a3dd0de4-8188-4117-9e8b-ecc5eb448096.xml, devinst.cm_free_res_des_handle
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CM_NOTIFY_ACTION, *PCM_NOTIFY_ACTION
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
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
---

# CM_Free_Res_Des_Handle function


## -description


The <b>CM_Free_Res_Des_Handle</b> function invalidates a resource description handle and frees its associated memory allocation.


## -parameters




### -param rdResDes [in]

Caller-supplied resource descriptor handle to be freed. This handle must have been previously obtained by calling one of the following functions:


<a href="https://msdn.microsoft.com/library/windows/hardware/ff537939">CM_Add_Res_Des</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537941">CM_Add_Res_Des_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538600">CM_Get_Next_Res_Des</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538603">CM_Get_Next_Res_Des_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538763">CM_Modify_Res_Des</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538775">CM_Modify_Res_Des_Ex</a>



## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



Each time your code calls one of the functions listed under the description of <i>rdResDes</i>, it must subsequently call <b>CM_Free_Res_Des_Handle</b>.



