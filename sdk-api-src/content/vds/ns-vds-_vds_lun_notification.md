---
UID: NS:vds._VDS_LUN_NOTIFICATION
title: "_VDS_LUN_NOTIFICATION"
author: windows-sdk-content
description: Defines the details of a LUN notification.
old-location: base\vds_lun_notification.htm
tech.root: vds
ms.assetid: 42b71b32-337e-4352-b4b3-6af2caad86e5
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: VDS_LUN_NOTIFICATION, VDS_LUN_NOTIFICATION structure [VDS], VDS_NF_LUN_ARRIVE, VDS_NF_LUN_DEPART, VDS_NF_LUN_MODIFY, _VDS_LUN_NOTIFICATION, base.vds_lun_notification, vds/_VDS_LUN_NOTIFICATION, vdshwprv/_VDS_LUN_NOTIFICATION
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_LUN_NOTIFICATION
product: Windows
targetos: Windows
req.typenames: VDS_LUN_NOTIFICATION
req.redist: 
---

# _VDS_LUN_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines 
   the details of a LUN notification.


## -struct-fields




### -field ulEvent


Determines the LUN event for which an application will be notified, as one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_LUN_ARRIVE"></a><a id="vds_nf_lun_arrive"></a><dl>
<dt><b><b>VDS_NF_LUN_ARRIVE</b></b></dt>
<dt>108</dt>
</dl>
</td>
<td width="60%">
A new LUN has been created.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_LUN_DEPART"></a><a id="vds_nf_lun_depart"></a><dl>
<dt><b><b>VDS_NF_LUN_DEPART</b></b></dt>
<dt>109</dt>
</dl>
</td>
<td width="60%">
An existing LUN has been deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_LUN_MODIFY"></a><a id="vds_nf_lun_modify"></a><dl>
<dt><b><b>VDS_NF_LUN_MODIFY</b></b></dt>
<dt>110</dt>
</dl>
</td>
<td width="60%">
A member was changed in the <a href="https://msdn.microsoft.com/4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a">VDS_LUN_PROP</a> 
       structure for an external LUN. Examples of changes that trigger this notification include changes to the 
        <b>VDS_LUN_PROP</b>structure and the addition of a plex to 
        the LUN. Applications are responsible for determining the precise nature of the change.

</td>
</tr>
</table>
 


### -field LunId

The GUID of the LUN.


## -remarks



This structure is included as a member in the 
    <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure.

An application can receive LUN events by implementing the 
    <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the 
    <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> method.

To get the LUN object, use the <a href="https://msdn.microsoft.com/622a95a4-0e8c-4f65-a935-61cb48379065">IVdsService::GetObject</a> method. You can then use the <a href="https://msdn.microsoft.com/1fec1c8d-7ac9-4b77-830c-930908aac6ef">IVdsLun::GetProperties</a> method to get the LUN properties.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>
 

 

