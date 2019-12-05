---
UID: NS:vdshwprv._VDS_WWN
title: VDS_WWN (vdshwprv.h)
description: Defines a world-wide name (WWN). This structure corresponds to the HBA_WWN structure defined by the ANSI HBA API.
old-location: base\vds_wwn.htm
tech.root: VDS
ms.assetid: a6d546bd-26ba-4f49-aeed-1f5462cc0bab
ms.date: 12/05/2018
ms.keywords: VDS_WWN, VDS_WWN structure [VDS], base.vds_wwn, vds/VDS_WWN, vdshwprv/VDS_WWN
ms.topic: struct
f1_keywords:
- vdshwprv/VDS_WWN
dev_langs:
- c++
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
- VDS_WWN
targetos: Windows
req.typenames: VDS_WWN
req.redist: 
ms.custom: 19H1
---

# VDS_WWN structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines a world-wide name (WWN). This 
   structure corresponds to the HBA_WWN structure defined by the ANSI HBA API.


## -struct-fields




### -field rguchWwn

An array of 8 bytes that together specify the 64-bit WWN value. The first element of the array is the most 
      significant byte of the WWN, with the most significant bit of that byte being the most significant bit of the 
      WWN.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hbaport_prop">VDS_HBAPORT_PROP</a>
 

 

