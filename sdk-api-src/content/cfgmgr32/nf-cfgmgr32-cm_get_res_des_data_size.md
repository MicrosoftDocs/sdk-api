---
UID: NF:cfgmgr32.CM_Get_Res_Des_Data_Size
title: CM_Get_Res_Des_Data_Size function (cfgmgr32.h)
author: windows-sdk-content
description: The CM_Get_Res_Des_Data_Size function obtains the buffer size required to hold the information contained in a specified resource descriptor on the local machine.
old-location: devinst\cm_get_res_des_data_size.htm
tech.root: devinst
ms.assetid: 51337d09-2ebb-45fd-82cd-2362093fb7ff
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CM_Get_Res_Des_Data_Size, CM_Get_Res_Des_Data_Size function [Device and Driver Installation], cfgmgr32/CM_Get_Res_Des_Data_Size, cfgmgrfn_bc279907-eb02-45fc-801d-48dde3d046a9.xml, devinst.cm_get_res_des_data_size
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
 - CM_Get_Res_Des_Data_Size
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Get_Res_Des_Data_Size function


## -description


The <b>CM_Get_Res_Des_Data_Size</b> function obtains the buffer size required to hold the information contained in a specified <a href="https://msdn.microsoft.com/004698f5-cb0e-4995-a19c-7075aa226000">resource descriptor</a> on the local machine.


## -parameters




### -param pulSize [out]

Caller-supplied address of a location to receive the required buffer size.


### -param rdResDes [in]

Caller-supplied handle to a resource descriptor, obtained by a previous call to <a href="https://msdn.microsoft.com/2ce2a84c-a9fe-42ff-920f-47dd0f54a820">CM_Get_Next_Res_Des</a>.


### -param ulFlags [in]

Not used, must be zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Get_Res_Des_Data_Size</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -remarks



The returned size value represents the size of the appropriate resource structure (see <a href="https://msdn.microsoft.com/0097b53a-c1c8-4e76-beef-812a953073b6">CM_Add_Res_Des</a>). If the resource descriptor resides in a resource requirements list, the returned size includes both the size of the resource structure and the space allocated for associated range arrays.




## -see-also




<a href="https://msdn.microsoft.com/59b96655-aea9-4f98-9f6a-1a9093db9c63">CM_Get_Res_Des_Data_Size_Ex</a>
 

 

