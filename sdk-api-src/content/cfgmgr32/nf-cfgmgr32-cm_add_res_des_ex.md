---
UID: NF:cfgmgr32.CM_Add_Res_Des_Ex
title: CM_Add_Res_Des_Ex function (cfgmgr32.h)
description: The CM_Add_Res_Des_Ex function adds a resource descriptor to a logical configuration. The logical configuration can be on either the local or a remote machine.helpviewer_keywords: ["CM_Add_Res_Des_Ex","CM_Add_Res_Des_Ex function [Device and Driver Installation]","cfgmgr32/CM_Add_Res_Des_Ex","cfgmgrfn_b3ed76ba-a2cc-4ede-a079-6e39c5c1d3bd.xml","devinst.cm_add_res_des_ex"]
old-location: devinst\cm_add_res_des_ex.htm
tech.root: devinst
ms.assetid: f19996ae-f243-4e8c-b200-7d11c06490c9
ms.date: 12/05/2018
ms.keywords: CM_Add_Res_Des_Ex, CM_Add_Res_Des_Ex function [Device and Driver Installation], cfgmgr32/CM_Add_Res_Des_Ex, cfgmgrfn_b3ed76ba-a2cc-4ede-a079-6e39c5c1d3bd.xml, devinst.cm_add_res_des_ex
f1_keywords:
- cfgmgr32/CM_Add_Res_Des_Ex
dev_langs:
- c++
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
- CM_Add_Res_Des_Ex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CM_Add_Res_Des_Ex function


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, this function has been deprecated.  Please use <a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_res_des">CM_Add_Res_Des</a> instead.]

The <b>CM_Add_Res_Des_Ex</b> function adds a <a href="https://docs.microsoft.com/windows-hardware/drivers/">resource descriptor</a> to a <a href="https://docs.microsoft.com/windows-hardware/drivers/kernel/hardware-resources">logical configuration</a>. The logical configuration can be on either the local or a remote machine.


## -parameters




### -param prdResDes [out, optional]

Pointer to a location to receive a handle to the new resource descriptor.


### -param lcLogConf [in]

Caller-supplied handle to the logical configuration to which the resource descriptor should be added. This handle must have been previously obtained by calling one of the following functions:


<a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf">CM_Add_Empty_Log_Conf</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_empty_log_conf_ex">CM_Add_Empty_Log_Conf_Ex</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf">CM_Get_First_Log_Conf</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_first_log_conf_ex">CM_Get_First_Log_Conf_Ex</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf">CM_Get_Next_Log_Conf</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_get_next_log_conf_ex">CM_Get_Next_Log_Conf_Ex</a>



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

[BUSNUMBER_RESOURCE](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-busnumber_resource)a>


</td>
</tr>
<tr>
<td>
<b>ResType_ClassSpecific</b>

</td>
<td>

[CS_RESOURCE](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-cs_resource)a>


</td>
</tr>
<tr>
<td>
<b>ResType_DevicePrivate</b>

</td>
<td>

<a href="https://docs.microsoft.com/windows-hardware/drivers/install/devprivate-resource">DEVPRIVATE_RESOURCE</a>


</td>
</tr>
<tr>
<td>
<b>ResType_DMA</b>

</td>
<td>

[DMA_RESOURCE](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-dma_resource)a>


</td>
</tr>
<tr>
<td>
<b>ResType_IO</b>

</td>
<td>

[IO_RESOURCE](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_resource)a>


</td>
</tr>
<tr>
<td>
<b>ResType_IRQ</b>

</td>
<td>

[IRQ_RESOURCE](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-irq_resource_32)a>


</td>
</tr>
<tr>
<td>
<b>ResType_Mem</b>

</td>
<td>

[MEM_RESOURCE](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mem_resource)a>


</td>
</tr>
<tr>
<td>
<b>ResType_MfCardConfig</b>

</td>
<td>

[MFCARD_RESOURCE](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-mfcard_resource)a>


</td>
</tr>
<tr>
<td>
<b>ResType_PcCardConfig</b>

</td>
<td>

[PCCARD_RESOURCE](https://docs.microsoft.com/windows/desktop/api/cfgmgr32/ns-cfgmgr32-pccard_resource)a>


</td>
</tr>
</table>
 


### -param ResourceLen [in]

Caller-supplied length of the structure pointed to by <i>ResourceData</i>.


### -param ulFlags [in]

Not used, must be zero.


### -param hMachine [in, optional]

Caller-supplied machine handle, obtained from a previous call to <a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_connect_machinew">CM_Connect_Machine</a>, or <b>NULL</b>.

<div class="alert"><b>Note</b>  Using this function to access remote machines is not supported beginning with Windows 8 and Windows Server 2012, as this functionality has been removed.</div>
<div> </div>

## -returns



If the operation succeeds, the function returns CR_SUCCESS. Otherwise, it returns one of the CR_-prefixed error codes defined in <i>Cfgmgr32.h</i>.

<div class="alert"><b>Note</b>  Starting with Windows 8, <b>CM_Add_Res_Des_Ex</b> returns CR_CALL_NOT_IMPLEMENTED when used in a Wow64 scenario. To request information about the hardware resources on a local machine it is necessary implement an architecture-native version of the application using the hardware resource APIs. For example: An AMD64 application for AMD64 systems.</div>
<div> </div>



## -remarks



Callers of <b>CM_Add_Res_Des_Ex</b> must call <a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle">CM_Free_Res_Des_Handle</a> to deallocate the resource descriptor handle, after it is no longer needed.

Callers of this function must have <b>SeLoadDriverPrivilege</b>. (Privileges are described in the Microsoft Windows SDK documentation.)

Functionality to access remote machines has been removed in Windows 8 and Windows Server 2012 and later operating systems thus you cannot access remote machines when running on these versions of Windows.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_add_res_des">CM_Add_Res_Des</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cfgmgr32/nf-cfgmgr32-cm_free_res_des_handle">CM_Free_Res_Des_Handle</a>
 

 

