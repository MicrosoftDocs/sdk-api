---
UID: NF:cfgmgr32.CM_Free_Log_Conf_Handle
title: CM_Free_Log_Conf_Handle function
author: windows-sdk-content
description: The CM_Free_Log_Conf_Handle function invalidates a logical configuration handle and frees its associated memory allocation.
old-location: devinst\cm_free_log_conf_handle.htm
tech.root: devinst
ms.assetid: dd8a4a2a-9f99-48c0-acb6-e5ceed63c88e
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CM_Free_Log_Conf_Handle, CM_Free_Log_Conf_Handle function [Device and Driver Installation], cfgmgr32/CM_Free_Log_Conf_Handle, cfgmgrfn_acfb6a9e-f12b-40af-a239-dba8aff1e22b.xml, devinst.cm_free_log_conf_handle
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
 - CM_Free_Log_Conf_Handle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CM_Free_Log_Conf_Handle
: 
---

# CM_Free_Log_Conf_Handle function


## -description


The <b>CM_Free_Log_Conf_Handle</b> function invalidates a logical configuration handle and frees its associated memory allocation.


## -parameters




### -param lcLogConf [in]

Caller-supplied logical configuration handle. This handle must have been previously obtained by calling one of the following functions:


<a href="https://msdn.microsoft.com/9de0b04d-96be-4c93-b7af-09200fdcf807">CM_Add_Empty_Log_Conf</a>



<a href="https://msdn.microsoft.com/cb34e5ec-4257-4c30-890a-40f669f1dfeb">CM_Add_Empty_Log_Conf_Ex</a>



<a href="https://msdn.microsoft.com/7ef14797-ea67-40cb-ad8d-e8c846ae1fd4">CM_Get_First_Log_Conf</a>



<a href="https://msdn.microsoft.com/cb562b5c-eb40-4be4-89a3-0e69a78ae6ea">CM_Get_First_Log_Conf_Ex</a>



<a href="https://msdn.microsoft.com/fa256bda-a7ee-4583-a91b-e7c2ef39b3f2">CM_Get_Next_Log_Conf</a>



<a href="https://msdn.microsoft.com/590baeb8-9234-4895-a05b-1917b2ee0155">CM_Get_Next_Log_Conf_Ex</a>



## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



Each time your code calls one of the functions listed under the description of <i>lcLogConf</i>, it must subsequently call <b>CM_Free_Log_Conf_Handle</b>.



