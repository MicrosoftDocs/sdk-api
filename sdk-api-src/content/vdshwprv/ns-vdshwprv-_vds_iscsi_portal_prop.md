---
UID: NS:vdshwprv._VDS_ISCSI_PORTAL_PROP
title: "_VDS_ISCSI_PORTAL_PROP"
author: windows-sdk-content
description: Defines the properties of an iSCSI portal.
old-location: base\vds_iscsi_portal_prop.htm
old-project: VDS
ms.assetid: da2d19ca-88a8-4a6a-bbe7-98a9d8af5b1b
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PVDS_ISCSI_PORTAL_PROP, VDS_ISCSI_PORTAL_PROP, VDS_ISCSI_PORTAL_PROP structure [VDS], _VDS_ISCSI_PORTAL_PROP, base.vds_iscsi_portal_prop, vds/VDS_ISCSI_PORTAL_PROP, vdshwprv/VDS_ISCSI_PORTAL_PROP"
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
req.typenames: VDS_ISCSI_PORTAL_PROP, *PVDS_ISCSI_PORTAL_PROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
-	VdsHwPrv.h
api_name:
-	VDS_ISCSI_PORTAL_PROP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_ISCSI_PORTAL_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of an iSCSI portal.


## -struct-fields




### -field id

The <b>VDS_OBJECT_ID</b> of the portal.


### -field address

The IP address and port of the portal.


### -field status


     The status of the portal, enumerated by 
     <a href="https://msdn.microsoft.com/ae39dfb8-6519-4307-8038-3af670553f51">VDS_ISCSI_PORTAL_STATUS</a>.


## -see-also




<a href="https://msdn.microsoft.com/a17597d5-2525-4a0c-acb3-dc69a6ef04ce">IVdsIscsiPortal::GetProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/42e8b161-5e47-4aae-aa23-94b5cacb5698">VDS_IPADDRESS</a>



<a href="https://msdn.microsoft.com/ae39dfb8-6519-4307-8038-3af670553f51">VDS_ISCSI_PORTAL_STATUS</a>
 

 

