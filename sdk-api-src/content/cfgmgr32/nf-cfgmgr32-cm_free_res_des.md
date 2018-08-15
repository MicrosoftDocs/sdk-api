---
UID: NF:cfgmgr32.CM_Free_Res_Des
title: CM_Free_Res_Des function
author: windows-sdk-content
description: The CM_Free_Res_Des function removes a resource descriptor from a logical configuration on the local machine.
old-location: devinst\cm_free_res_des.htm
old-project: devinst
ms.assetid: baef66ed-11a9-4a54-ba07-82159a9101e7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CM_Free_Res_Des, CM_Free_Res_Des function [Device and Driver Installation], cfgmgr32/CM_Free_Res_Des, cfgmgrfn_57d3d070-5730-4c20-a558-a52855e4d1e1.xml, devinst.cm_free_res_des
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.redist: 
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
 - CM_Free_Res_Des
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
---

# CM_Free_Res_Des function


## -description


The <b>CM_Free_Res_Des</b> function removes a <a href="https://msdn.microsoft.com/004698f5-cb0e-4995-a19c-7075aa226000">resource descriptor</a> from a <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">logical configuration</a> on the local machine.


## -parameters




### -param prdResDes [out]

Caller-supplied location to receive a handle to the configuration's previous resource descriptor. This parameter can be <b>NULL</b>. For more information, see the following <b>Remarks</b> section.


### -param rdResDes [in]

Caller-supplied handle to the resource descriptor to be removed. This handle must have been previously obtained by calling one of the following functions:


<a href="https://msdn.microsoft.com/0097b53a-c1c8-4e76-beef-812a953073b6">CM_Add_Res_Des</a>



<a href="https://msdn.microsoft.com/f19996ae-f243-4e8c-b200-7d11c06490c9">CM_Add_Res_Des_Ex</a>



<a href="https://msdn.microsoft.com/2ce2a84c-a9fe-42ff-920f-47dd0f54a820">CM_Get_Next_Res_Des</a>



<a href="https://msdn.microsoft.com/91e9a686-2465-4ae8-9cc2-391cd98c2138">CM_Get_Next_Res_Des_Ex</a>



<a href="https://msdn.microsoft.com/9320c396-4da8-4b35-a620-4bb7cbd80e9a">CM_Modify_Res_Des</a>



<a href="https://msdn.microsoft.com/6bb4af46-995e-4487-9c5f-89c72abb0ec5">CM_Modify_Res_Des_Ex</a>



### -param ulFlags [in]

Not used, must be zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Free_Res_Des</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -remarks



Resource descriptors for each configuration are stored in an array. If you specify an address for <i>prdResDes</i>, then <b>CM_Free_Res_Des</b> returns a handle to the resource descriptor that was previous, in the array, to the one removed. If the handle specified by <i>rdResDes</i> represents the resource descriptor located first in the array, then <i>prdResDes</i> receives a handle to the logical configuration.

Note that calling <b>CM_Free_Res_Des</b> frees the resource descriptor, but not the descriptor's handle. To free the handle, call <b>CM_Free_Res_Des_Handle</b>.

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)




## -see-also




<a href="https://msdn.microsoft.com/2c6768c2-183b-480d-96cf-0f62f33d62d1">CM_Free_Res_Des_Ex</a>
 

 

