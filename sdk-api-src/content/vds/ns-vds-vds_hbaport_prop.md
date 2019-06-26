---
UID: NS:vds._VDS_HBAPORT_PROP
title: VDS_HBAPORT_PROP (vds.h)
author: windows-sdk-content
description: Defines the properties of an HBA port.
old-location: base\vds_hbaport_prop.htm
tech.root: VDS
ms.assetid: 297ccb5c-3fa2-4bb0-bdd2-60d4685dc55c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VDS_HBAPORT_PROP, VDS_HBAPORT_PROP structure [VDS], base.vds_hbaport_prop, vds/VDS_HBAPORT_PROP, vdshwprv/VDS_HBAPORT_PROP
ms.topic: struct
f1_keywords: 
 - "vds/VDS_HBAPORT_PROP"
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
 - VDS_HBAPORT_PROP
product: Windows
targetos: Windows
req.typenames: VDS_HBAPORT_PROP
req.redist: 
ms.custom: 19H1
---

# VDS_HBAPORT_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
    properties of an HBA port.


## -struct-fields




### -field id

The GUID assigned to the HBA port. This ID is used by the VDS service only; hardware providers should 
      ignore this field.


### -field wwnNode

The node WWN of the HBA port.


### -field wwnPort

The port WWN of the HBA port.


### -field type

The type of the HBA port enumerated by 
      <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-_vds_hbaport_type">VDS_HBAPORT_TYPE</a>.


### -field status

The status of the HBA port enumerated by 
      <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-_vds_hbaport_status">VDS_HBAPORT_STATUS</a>.


### -field ulPortSpeed

The speed of the HBA port enumerated by 
      <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-_vds_hbaport_speed_flag">VDS_HBAPORT_SPEED_FLAG</a>.


### -field ulSupportedPortSpeed

The set of supported speeds of the HBA port, one bit set for each of the supported speeds  enumerated by 
      <a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-_vds_hbaport_speed_flag">VDS_HBAPORT_SPEED_FLAG</a>.
     


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-_vds_hbaport_speed_flag">VDS_HBAPORT_SPEED_FLAG</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-_vds_hbaport_status">VDS_HBAPORT_STATUS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-_vds_hbaport_type">VDS_HBAPORT_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-_vds_wwn">VDS_WWN</a>
 

 

