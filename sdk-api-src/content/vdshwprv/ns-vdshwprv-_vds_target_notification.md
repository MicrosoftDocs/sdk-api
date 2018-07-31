---
UID: NS:vdshwprv._VDS_TARGET_NOTIFICATION
title: "_VDS_TARGET_NOTIFICATION"
author: windows-sdk-content
description: Defines the details of iSCSI target events.
old-location: base\vds_target_notification.htm
old-project: VDS
ms.assetid: 71453c9c-d6a7-4527-8988-c0388d7a9991
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: VDS_NF_TARGET_ARRIVE, VDS_NF_TARGET_DEPART, VDS_NF_TARGET_MODIFY, VDS_TARGET_NOTIFICATION, VDS_TARGET_NOTIFICATION structure [VDS], _VDS_TARGET_NOTIFICATION, base.vds_target_notification, vds/_VDS_TARGET_NOTIFICATION, vdshwprv/_VDS_TARGET_NOTIFICATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: VDS_TARGET_NOTIFICATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_TARGET_NOTIFICATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_TARGET_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the details of iSCSI target events.


## -struct-fields




### -field ulEvent

Determines the iSCSI target event for which an application will be notified, as one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_TARGET_ARRIVE"></a><a id="vds_nf_target_arrive"></a><dl>
<dt><b>VDS_NF_TARGET_ARRIVE</b></dt>
<dt>126</dt>
</dl>
</td>
<td width="60%">
An iSCSI target has been created.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_TARGET_DEPART"></a><a id="vds_nf_target_depart"></a><dl>
<dt><b>VDS_NF_TARGET_DEPART</b></dt>
<dt>127</dt>
</dl>
</td>
<td width="60%">
An existing iSCSI target has been deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_TARGET_MODIFY"></a><a id="vds_nf_target_modify"></a><dl>
<dt><b>VDS_NF_TARGET_MODIFY</b></dt>
<dt>128</dt>
</dl>
</td>
<td width="60%">
An existing iSCSI target has changed. An example of change that triggers this notification would be
        changes to the <a href="https://msdn.microsoft.com/ca92c9e8-4d15-4b3c-8420-3eac18a7c2f5">VDS_ISCSI_TARGET_PROP</a> 
        structure. Applications are responsible for determining the nature of any changes.

</td>
</tr>
</table>
 


### -field targetId

The <b>VDS_OBJECT_ID</b> of the iSCSI target that triggered the event.


## -remarks



The <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive disk events by implementing the 
    <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> 
    method.

To get the iSCSI target object, use the <a href="https://msdn.microsoft.com/622a95a4-0e8c-4f65-a935-61cb48379065">IVdsService::GetObject</a> method. You can then use the <a href="https://msdn.microsoft.com/db48ec8e-aae1-4b88-9942-6a23de2cfe25">IVdsIscsiTarget::GetProperties</a> method to get the target properties.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/0db442c4-6cc1-43b2-8ac8-8b17cadb1101">IVdsIscsiTarget</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/ca92c9e8-4d15-4b3c-8420-3eac18a7c2f5">VDS_ISCSI_TARGET_PROP</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>
 

 

