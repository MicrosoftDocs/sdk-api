---
UID: NS:vds._VDS_PATH_ID
title: VDS_PATH_ID (vds.h)
description: The VDS_PATH_ID structure (vds.h) defines a unique identification for a path.  
helpviewer_keywords: ["VDS_PATH_ID","VDS_PATH_ID structure [VDS]","base.vds_path_id","vds/VDS_PATH_ID","vdshwprv/VDS_PATH_ID"]
old-location: base\vds_path_id.htm
tech.root: base
ms.assetid: bfb786fc-eb03-4449-b631-fb85813c08c8
ms.date: 08/05/2022
ms.keywords: VDS_PATH_ID, VDS_PATH_ID structure [VDS], base.vds_path_id, vds/VDS_PATH_ID, vdshwprv/VDS_PATH_ID
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
targetos: Windows
req.typenames: VDS_PATH_ID
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_PATH_ID
 - vds/_VDS_PATH_ID
 - VDS_PATH_ID
 - vds/VDS_PATH_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_PATH_ID
---

# VDS_PATH_ID structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines a unique 
   identification for a path.

## -struct-fields

### -field ullSourceId

The source ID for the path. If this is an 
      MPIO path, the source ID is the unique DSM ID.

### -field ullPathId

The ID of the path given by the MPIO DSM.

## -see-also

<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_path_info">VDS_PATH_INFO</a>
