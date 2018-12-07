---
UID: NS:vds._VDS_ISCSI_INITIATOR_PORTAL_PROP
title: "_VDS_ISCSI_INITIATOR_PORTAL_PROP"
author: windows-sdk-content
description: Defines the properties of an iSCSI initiator portal.
old-location: base\vds_iscsi_initiator_portal_prop.htm
tech.root: vds
ms.assetid: 58fffdb4-71c4-4f84-ad0e-7efe5bdb78a7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VDS_ISCSI_INITIATOR_PORTAL_PROP, VDS_ISCSI_INITIATOR_PORTAL_PROP structure [VDS], _VDS_ISCSI_INITIATOR_PORTAL_PROP, base.vds_iscsi_initiator_portal_prop, vds/VDS_ISCSI_INITIATOR_PORTAL_PROP, vdshwprv/VDS_ISCSI_INITIATOR_PORTAL_PROP
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - VDS_ISCSI_INITIATOR_PORTAL_PROP
product: Windows
targetos: Windows
req.typenames: VDS_ISCSI_INITIATOR_PORTAL_PROP
req.redist: VDS 1.1
---

# _VDS_ISCSI_INITIATOR_PORTAL_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of an iSCSI initiator portal.


## -struct-fields




### -field id

The <b>VDS_OBJECT_ID</b> assigned to the initiator portal.


### -field address

The IP address and port of the portal.


### -field ulPortIndex

The port index assigned to the portal by the iSCSI initiator service.


## -see-also




<a href="https://msdn.microsoft.com/7bf00853-ca26-40b4-a09a-dcb5e7e08f49">IVdsIscsiInitiatorPortal::GetProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/42e8b161-5e47-4aae-aa23-94b5cacb5698">VDS_IPADDRESS</a>
 

 

