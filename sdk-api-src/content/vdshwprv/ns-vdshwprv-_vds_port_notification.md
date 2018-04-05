---
UID: NS:vdshwprv._VDS_PORT_NOTIFICATION
title: "_VDS_PORT_NOTIFICATION"
author: windows-driver-content
description: Defines the details of controller port events.
old-location: base\vds_port_notification.htm
old-project: VDS
ms.assetid: 4de0969f-fed5-42c7-a5f8-0bd6c58dc237
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: VDS_NF_PORT_ARRIVE, VDS_NF_PORT_DEPART, VDS_NF_PORT_MODIFY, VDS_NF_PORT_REMOVED, VDS_PORT_NOTIFICATION, VDS_PORT_NOTIFICATION structure [VDS], _VDS_PORT_NOTIFICATION, base.vds_port_notification, vds/_VDS_PORT_NOTIFICATION, vdshwprv/_VDS_PORT_NOTIFICATION
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VDS_PORT_NOTIFICATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
-	VdsHwPrv.h
api_name:
-	VDS_PORT_NOTIFICATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_PORT_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines 
   the details of controller port events.


## -struct-fields




### -field ulEvent

Determines the controller port event for which an application will be notified, as one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORT_ARRIVE"></a><a id="vds_nf_port_arrive"></a><dl>
<dt><b>VDS_NF_PORT_ARRIVE</b></dt>
<dt>121</dt>
</dl>
</td>
<td width="60%">
A controller port is reported as physically present on the subsystem. 
The <a href="https://msdn.microsoft.com/6e363020-caf4-4028-abd5-7f311edb2e69">VDS_PORT_STATUS</a> value associated with this notification should be any value except <b>VDS_PRS_REMOVED</b>.


</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORT_DEPART"></a><a id="vds_nf_port_depart"></a><dl>
<dt><b>VDS_NF_PORT_DEPART</b></dt>
<dt>122</dt>
</dl>
</td>
<td width="60%">
A controller, and therefore its port, were physically unplugged from the subsystem. The <a href="https://msdn.microsoft.com/6e363020-caf4-4028-abd5-7f311edb2e69">VDS_PORT_STATUS</a> value should be <b>VDS_PRS_UNKNOWN</b> or <b>VDS_PRS_REMOVED</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORT_MODIFY"></a><a id="vds_nf_port_modify"></a><dl>
<dt><b>VDS_NF_PORT_MODIFY</b></dt>
<dt>352</dt>
</dl>
</td>
<td width="60%">
A member of the <a href="https://msdn.microsoft.com/40f81f31-3776-4685-8b79-c047c669b2bb">VDS_PORT_PROP</a> structure changed.

<b>Windows Server 2008, Windows Vista and Windows Server 2003 R2:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PORT_REMOVED"></a><a id="vds_nf_port_removed"></a><dl>
<dt><b>VDS_NF_PORT_REMOVED</b></dt>
<dt>353</dt>
</dl>
</td>
<td width="60%">
A controller port is physically present but not available for use. For example, either the controller or the port itself is set to inactive. The <a href="https://msdn.microsoft.com/6e363020-caf4-4028-abd5-7f311edb2e69">VDS_PORT_STATUS</a> value should be <b>VDS_PRS_FAILED</b>  (removed from use because of failure), <b>VDS_PRS_OFFLINE</b>  (not failed, but not in use either), <b>VDS_PRS_NOT_READY</b>, or <b>VDS_PRS_UNKNOWN</b>.

<b>Windows Server 2008, Windows Vista and Windows Server 2003 R2:  </b>This value is not supported.

</td>
</tr>
</table>
 


### -field portId

The <b>VDS_OBJECT_ID</b> of the controller port that triggered the event.


## -remarks



The <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive disk events by implementing the 
    <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> 
    method.

To get the port object, use the <a href="https://msdn.microsoft.com/622a95a4-0e8c-4f65-a935-61cb48379065">IVdsService::GetObject</a> method. You can then use the <a href="https://msdn.microsoft.com/7540f2d3-c17c-4868-9e72-116219bab51c">IVdsControllerPort::GetProperties</a> method to get the port properties.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/a0ceaf1d-b839-4cf7-b64e-9100f3cf23ef">IVdsControllerPort</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>
 

 

