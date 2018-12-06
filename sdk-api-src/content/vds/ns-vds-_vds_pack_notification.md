---
UID: NS:vds._VDS_PACK_NOTIFICATION
title: "_VDS_PACK_NOTIFICATION"
author: windows-sdk-content
description: Defines the details of pack events.
old-location: base\vds_pack_notification.htm
tech.root: vds
ms.assetid: 3bfdef22-e3ad-4b23-9aaa-c2d08044dd25
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VDS_NF_PACK_ARRIVE, VDS_NF_PACK_DEPART, VDS_NF_PACK_MODIFY, VDS_PACK_NOTIFICATION, VDS_PACK_NOTIFICATION structure [VDS], _VDS_PACK_NOTIFICATION, base.vds_pack_notification, vds/_VDS_PACK_NOTIFICATION, vdshwprv/_VDS_PACK_NOTIFICATION
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
 - VDS_PACK_NOTIFICATION
product: Windows
targetos: Windows
req.typenames: VDS_PACK_NOTIFICATION
req.redist: 
---

# _VDS_PACK_NOTIFICATION structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines 
   the details of pack events.


## -struct-fields




### -field ulEvent

Determines the pack event for which an application will be notified, as one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PACK_ARRIVE"></a><a id="vds_nf_pack_arrive"></a><dl>
<dt><b>VDS_NF_PACK_ARRIVE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
A new pack arrived.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PACK_DEPART"></a><a id="vds_nf_pack_depart"></a><dl>
<dt><b>VDS_NF_PACK_DEPART</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
An existing pack was removed.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_NF_PACK_MODIFY"></a><a id="vds_nf_pack_modify"></a><dl>
<dt><b>VDS_NF_PACK_MODIFY</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
A member of the <a href="https://msdn.microsoft.com/5d04bf6c-fda2-4b95-a8bb-907e64267f30">VDS_PACK_PROP</a> 
       structure for the pack was changed.

</td>
</tr>
</table>
 


### -field packId

The GUID for the pack that triggered the event.


## -remarks



The <a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a> structure includes this 
    structure as a member.

An application can receive pack events by implementing the 
    <a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a> interface and passing the interface 
    pointer as an argument to the 
    <a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a> method.

To get the pack object, use the <a href="https://msdn.microsoft.com/622a95a4-0e8c-4f65-a935-61cb48379065">IVdsService::GetObject</a> method. You can then use the <a href="https://msdn.microsoft.com/0793642c-1905-470c-a69f-8bf5f8bbe90d">IVdsPack::GetProperties</a> method to get the pack properties.




## -see-also




<a href="https://msdn.microsoft.com/8e9b7c95-0b59-4268-a274-5d16812075a6">IVdsAdviseSink</a>



<a href="https://msdn.microsoft.com/be1d5385-6c72-4847-9ed7-4d2309a3e9ac">IVdsService::Advise</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/59d21cd3-1cff-47be-be98-f4c55f044306">VDS_NOTIFICATION</a>
 

 

