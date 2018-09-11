---
UID: NS:vds._VDS_PORTAL_GROUP_NOTIFICATION
title: "_VDS_PORTAL_GROUP_NOTIFICATION"
author: windows-sdk-content
description: Defines the details of iSCSI portal events.
old-location: base\vds_portal_group_notification.htm
tech.root: VDS
ms.assetid: db4f947b-996f-4aa0-aed6-0190f00ca58a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: VDS_NF_PORTAL_GROUP_ARRIVE, VDS_NF_PORTAL_GROUP_DEPART, VDS_NF_PORTAL_GROUP_MODIFY, VDS_PORTAL_GROUP_NOTIFICATION, VDS_PORTAL_GROUP_NOTIFICATION structure [VDS], _VDS_PORTAL_GROUP_NOTIFICATION, base.vds_portal_group_notification, vds/_VDS_PORTAL_GROUP_NOTIFICATION, vdshwprv/_VDS_PORTAL_GROUP_NOTIFICATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vds.h
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
 - VDS_PORTAL_GROUP_NOTIFICATION
product: Windows
targetos: Windows
req.typenames: VDS_PORTAL_GROUP_NOTIFICATION
req.redist: VDS 1.1
---

# _VDS_PORTAL_GROUP_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the details of iSCSI portal events.


## -struct-fields




### -field ulEvent

Determines the iSCSI portal group event for which an application will be notified, as one of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORTAL_GROUP_ARRIVE"></a><a id="vds_nf_portal_group_arrive"></a><dl>
<dt><b>VDS_NF_PORTAL_GROUP_ARRIVE</b></dt>
<dt>129</dt>
</dl>
</td>
<td width="60%">
An iSCSI portal group has been created.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORTAL_GROUP_DEPART"></a><a id="vds_nf_portal_group_depart"></a><dl>
<dt><b>VDS_NF_PORTAL_GROUP_DEPART</b></dt>
<dt>130</dt>
</dl>
</td>
<td width="60%">
An existing iSCSI portal group has been deleted.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORTAL_GROUP_MODIFY"></a><a id="vds_nf_portal_group_modify"></a><dl>
<dt><b>VDS_NF_PORTAL_GROUP_MODIFY</b></dt>
<dt>131</dt>
</dl>
</td>
<td width="60%">
An existing iSCSI portal group has changed. An example of change that triggers this notification would be 
        changes to the <a href="https://msdn.microsoft.com/82f891a2-432b-4503-8b5a-a79bea800525">VDS_ISCSI_PORTALGROUP_PROP</a> 
        structure. Applications are responsible for determining the nature of any changes.

</td>
</tr>
</table>
 


### -field portalGroupId

The <b>VDS_OBJECT_ID</b> of the iSCSI portal that triggered the event.


## -remarks



The <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive disk events by implementing the 
    <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> 
    method.

To get the portal group object, use the <a href="https://msdn.microsoft.com/622a95a4-0e8c-4f65-a935-61cb48379065">IVdsService::GetObject</a> method. You can then use the <a href="https://msdn.microsoft.com/7257101e-04a5-41d5-b4fa-401106610dcf">IVdsIscsiPortalGroup::GetProperties</a> method to get the portal group properties.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/1f3131a6-01ab-41e5-9e2f-6ffcdcd0e3a6">IVdsIscsiPortal</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/82f891a2-432b-4503-8b5a-a79bea800525">VDS_ISCSI_PORTALGROUP_PROP</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>
 

 

