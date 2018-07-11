---
UID: NS:vds._VDS_SUB_SYSTEM_NOTIFICATION
title: "_VDS_SUB_SYSTEM_NOTIFICATION"
author: windows-sdk-content
description: Defines the details of subsystem events.
old-location: base\vds_sub_system_notification.htm
old-project: vds
ms.assetid: 368e5b3d-11ba-400e-8dd0-929d45199dd9
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: VDS_NF_SUB_SYSTEM_ARRIVE, VDS_NF_SUB_SYSTEM_DEPART, VDS_NF_SUB_SYSTEM_MODIFY, VDS_SUB_SYSTEM_NOTIFICATION, VDS_SUB_SYSTEM_NOTIFICATION structure [VDS], _VDS_SUB_SYSTEM_NOTIFICATION, base.vds_sub_system_notification, vds/_VDS_SUB_SYSTEM_NOTIFICATION, vdshwprv/_VDS_SUB_SYSTEM_NOTIFICATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: VDS_SUB_SYSTEM_NOTIFICATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_SUB_SYSTEM_NOTIFICATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_SUB_SYSTEM_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the details of subsystem events.


## -struct-fields




### -field ulEvent

Determines the subsystem event for which an application will be notified, as one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_SUB_SYSTEM_ARRIVE"></a><a id="vds_nf_sub_system_arrive"></a><dl>
<dt><b>VDS_NF_SUB_SYSTEM_ARRIVE</b></dt>
<dt>101</dt>
</dl>
</td>
<td width="60%">
A new subsystem was connected to the server or network.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_SUB_SYSTEM_DEPART"></a><a id="vds_nf_sub_system_depart"></a><dl>
<dt><b>VDS_NF_SUB_SYSTEM_DEPART</b></dt>
<dt>102</dt>
</dl>
</td>
<td width="60%">
An existing subsystem was disconnected.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_SUB_SYSTEM_MODIFY"></a><a id="vds_nf_sub_system_modify"></a><dl>
<dt><b>VDS_NF_SUB_SYSTEM_MODIFY</b></dt>
<dt>151</dt>
</dl>
</td>
<td width="60%">
A member of the <a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a> 
        structure was changed.

</td>
</tr>
</table>
 


### -field subSystemId

The subsystem's GUID.


## -remarks



The <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive subsystem events by implementing the 
    <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the 
    <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> method.

To get the subsystem object, use the <a href="https://msdn.microsoft.com/622a95a4-0e8c-4f65-a935-61cb48379065">IVdsService::GetObject</a> method. You can then use the <a href="https://msdn.microsoft.com/cbcf1e14-7e3d-44e6-8c4a-afe927ed0f9d">IVdsSubSystem::GetProperties</a> method or the <a href="https://msdn.microsoft.com/1f2164a9-643d-4762-8a2e-31d5c277502e">IVdsSubSystem2::GetProperties2</a> methodto get the subsystem properties.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>



<a href="https://msdn.microsoft.com/8fecb874-5c59-4f55-b528-040ff9209612">VDS_SUB_SYSTEM_PROP</a>
 

 

