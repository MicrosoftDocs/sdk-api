---
UID: NF:cfgmgr32.CM_Free_Log_Conf_Handle
title: CM_Free_Log_Conf_Handle function
author: windows-sdk-content
description: The CM_Free_Log_Conf_Handle function invalidates a logical configuration handle and frees its associated memory allocation.
old-location: devinst\cm_free_log_conf_handle.htm
old-project: devinst
ms.assetid: dd8a4a2a-9f99-48c0-acb6-e5ceed63c88e
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: CM_Free_Log_Conf_Handle, CM_Free_Log_Conf_Handle function [Device and Driver Installation], cfgmgr32/CM_Free_Log_Conf_Handle, cfgmgrfn_acfb6a9e-f12b-40af-a239-dba8aff1e22b.xml, devinst.cm_free_log_conf_handle
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
 - CM_Free_Log_Conf_Handle
product: Windows
targetos: Windows
req.lib: Cfgmgr32.lib
req.dll: Cfgmgr32.dll
req.irql: 
---

# CM_Free_Log_Conf_Handle function


## -description


The <b>CM_Free_Log_Conf_Handle</b> function invalidates a logical configuration handle and frees its associated memory allocation.


## -parameters




### -param lcLogConf [in]

Caller-supplied logical configuration handle. This handle must have been previously obtained by calling one of the following functions:


<a href="https://msdn.microsoft.com/library/windows/hardware/ff537921">CM_Add_Empty_Log_Conf</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff537926">CM_Add_Empty_Log_Conf_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538522">CM_Get_First_Log_Conf</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538529">CM_Get_First_Log_Conf_Ex</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538591">CM_Get_Next_Log_Conf</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538598">CM_Get_Next_Log_Conf_Ex</a>



## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.




## -remarks



Each time your code calls one of the functions listed under the description of <i>lcLogConf</i>, it must subsequently call <b>CM_Free_Log_Conf_Handle</b>.



