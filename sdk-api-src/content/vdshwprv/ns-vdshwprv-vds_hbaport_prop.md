---
UID: NS:vdshwprv._VDS_HBAPORT_PROP
title: VDS_HBAPORT_PROP
author: windows-sdk-content
description: Defines the properties of an HBA port.
old-location: base\vds_hbaport_prop.htm
tech.root: VDS
ms.assetid: 297ccb5c-3fa2-4bb0-bdd2-60d4685dc55c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VDS_HBAPORT_PROP, VDS_HBAPORT_PROP structure [VDS], base.vds_hbaport_prop, vds/VDS_HBAPORT_PROP, vdshwprv/VDS_HBAPORT_PROP
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
---

# VDS_HBAPORT_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

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
      <a href="https://msdn.microsoft.com/fcad33c0-9a85-4180-b5de-fbef06e9e6e6">VDS_HBAPORT_TYPE</a>.


### -field status

The status of the HBA port enumerated by 
      <a href="https://msdn.microsoft.com/67ef9025-c929-476b-8644-7e085dff91c4">VDS_HBAPORT_STATUS</a>.


### -field ulPortSpeed

The speed of the HBA port enumerated by 
      <a href="https://msdn.microsoft.com/b44a51b5-7aca-4e95-88ec-60ff026c411f">VDS_HBAPORT_SPEED_FLAG</a>.


### -field ulSupportedPortSpeed

The set of supported speeds of the HBA port, one bit set for each of the supported speeds  enumerated by 
      <a href="https://msdn.microsoft.com/b44a51b5-7aca-4e95-88ec-60ff026c411f">VDS_HBAPORT_SPEED_FLAG</a>.
     


## -see-also




<a href="https://msdn.microsoft.com/b44a51b5-7aca-4e95-88ec-60ff026c411f">VDS_HBAPORT_SPEED_FLAG</a>



<a href="https://msdn.microsoft.com/67ef9025-c929-476b-8644-7e085dff91c4">VDS_HBAPORT_STATUS</a>



<a href="https://msdn.microsoft.com/fcad33c0-9a85-4180-b5de-fbef06e9e6e6">VDS_HBAPORT_TYPE</a>



<a href="https://msdn.microsoft.com/a6d546bd-26ba-4f49-aeed-1f5462cc0bab">VDS_WWN</a>
 

 

