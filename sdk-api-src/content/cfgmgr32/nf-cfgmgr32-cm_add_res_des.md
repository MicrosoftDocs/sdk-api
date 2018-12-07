---
UID: NF:cfgmgr32.CM_Add_Res_Des
title: CM_Add_Res_Des function
author: windows-sdk-content
description: The CM_Add_Res_Des function adds a resource descriptor to a logical configuration.
old-location: devinst\cm_add_res_des.htm
tech.root: devinst
ms.assetid: 0097b53a-c1c8-4e76-beef-812a953073b6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CM_Add_Res_Des, CM_Add_Res_Des function [Device and Driver Installation], cfgmgr32/CM_Add_Res_Des, cfgmgrfn_86ee6b93-0cdd-4f18-87c2-8c8d0c33d39f.xml, devinst.cm_add_res_des
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
 - CM_Add_Res_Des
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CM_Add_Res_Des function


## -description


The <b>CM_Add_Res_Des</b> function adds a <a href="https://msdn.microsoft.com/004698f5-cb0e-4995-a19c-7075aa226000">resource descriptor</a> to a <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">logical configuration</a>.


## -parameters




### -param prdResDes [out, optional]

Pointer to a location to receive a handle to the new resource descriptor.


### -param lcLogConf [in]

Caller-supplied handle to the logical configuration to which the resource descriptor should be added. This handle must have been previously obtained by calling one of the following functions:


<a href="https://msdn.microsoft.com/9de0b04d-96be-4c93-b7af-09200fdcf807">CM_Add_Empty_Log_Conf</a>



<a href="https://msdn.microsoft.com/cb34e5ec-4257-4c30-890a-40f669f1dfeb">CM_Add_Empty_Log_Conf_Ex</a>



<a href="https://msdn.microsoft.com/7ef14797-ea67-40cb-ad8d-e8c846ae1fd4">CM_Get_First_Log_Conf</a>



<a href="https://msdn.microsoft.com/cb562b5c-eb40-4be4-89a3-0e69a78ae6ea">CM_Get_First_Log_Conf_Ex</a>



<a href="https://msdn.microsoft.com/fa256bda-a7ee-4583-a91b-e7c2ef39b3f2">CM_Get_Next_Log_Conf</a>



<a href="https://msdn.microsoft.com/590baeb8-9234-4895-a05b-1917b2ee0155">CM_Get_Next_Log_Conf_Ex</a>



### -param ResourceID [in]

Caller-supplied resource type identifier, which identifies the type of structure supplied by <i>ResourceData</i>. This must be one of the <b>ResType_</b>-prefixed constants defined in <i>Cfgmgr32.h</i>.


### -param ResourceData [in]

Caller-supplied pointer to one of the resource structures listed in the following table.

<table>
<tr>
<th><i>ResourceID </i>Parameter</th>
<th>Resource Structure</th>
</tr>
<tr>
<td>
<b>ResType_BusNumber</b>

</td>
<td>

<a href="https://msdn.microsoft.com/8dbf5499-8e43-4db9-b0ec-6536f1c6121c">BUSNUMBER_RESOURCE</a>


</td>
</tr>
<tr>
<td>
<b>ResType_ClassSpecific</b>

</td>
<td>

<a href="https://msdn.microsoft.com/471112ab-8f3b-4bfe-b456-68fea933a31f">CS_RESOURCE</a>


</td>
</tr>
<tr>
<td>
<b>ResType_DevicePrivate</b>

</td>
<td>

<a href="https://msdn.microsoft.com/842d9092-f7b6-4111-88d9-64a580007295">DEVPRIVATE_RESOURCE</a>


</td>
</tr>
<tr>
<td>
<b>ResType_DMA</b>

</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff544764(v=VS.85).aspx">DMA_RESOURCE</a>


</td>
</tr>
<tr>
<td>
<b>ResType_IO</b>

</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff548201(v=VS.85).aspx">IO_RESOURCE</a>


</td>
</tr>
<tr>
<td>
<b>ResType_IRQ</b>

</td>
<td>

<a href="https://msdn.microsoft.com/en-us/library/Ff548229(v=VS.85).aspx">IRQ_RESOURCE</a>


</td>
</tr>
<tr>
<td>
<b>ResType_Mem</b>

</td>
<td>

<a href="https://msdn.microsoft.com/42ecd736-abd3-4ac8-82bb-6bb69af1d96d">MEM_RESOURCE</a>


</td>
</tr>
<tr>
<td>
<b>ResType_MfCardConfig</b>

</td>
<td>

<a href="https://msdn.microsoft.com/26dbefb6-bc5c-4060-902d-3fd1adf833cb">MFCARD_RESOURCE</a>


</td>
</tr>
<tr>
<td>
<b>ResType_PcCardConfig</b>

</td>
<td>

<a href="https://msdn.microsoft.com/41f88d8f-2e1d-447d-90e2-6a2a5f7bef6f">PCCARD_RESOURCE</a>


</td>
</tr>
</table>
 


### -param ResourceLen [in]

Caller-supplied length of the structure pointed to by <i>ResourceData</i>.


### -param ulFlags [in]

Not used, must be zero.


## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8,  <b>CM_Add_Res_Des</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -remarks



Callers of <b>CM_Add_Res_Des</b> must call <a href="https://msdn.microsoft.com/4a585d64-fd00-47a8-8ada-7e343beb829d">CM_Free_Res_Des_Handle</a> to deallocate the resource descriptor handle, after it is no longer needed.

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)




## -see-also




<a href="https://msdn.microsoft.com/f19996ae-f243-4e8c-b200-7d11c06490c9">CM_Add_Res_Des_Ex</a>



<a href="https://msdn.microsoft.com/4a585d64-fd00-47a8-8ada-7e343beb829d">CM_Free_Res_Des_Handle</a>
 

 

