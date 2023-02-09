---
UID: NE:vdshwprv._VDS_LUN_PLEX_FLAG
title: VDS_LUN_PLEX_FLAG (vdshwprv.h)
description: The VDS_LUN_PLEX_FLAG enumeration (vdshwprv.h) defines the set of valid flags for a LUN plex object. 
helpviewer_keywords: ["VDS_LPF_LBN_REMAP_ENABLED","VDS_LUN_PLEX_FLAG","VDS_LUN_PLEX_FLAG enumeration [VDS]","base.vds_lun_plex_flag","vds/VDS_LPF_LBN_REMAP_ENABLED","vds/VDS_LUN_PLEX_FLAG","vdshwprv/VDS_LPF_LBN_REMAP_ENABLED","vdshwprv/VDS_LUN_PLEX_FLAG"]
old-location: base\vds_lun_plex_flag.htm
tech.root: base
ms.assetid: 0258d87c-0270-449e-8e96-2c511c5f7242
ms.date: 08/05/2022
ms.keywords: VDS_LPF_LBN_REMAP_ENABLED, VDS_LUN_PLEX_FLAG, VDS_LUN_PLEX_FLAG enumeration [VDS], base.vds_lun_plex_flag, vds/VDS_LPF_LBN_REMAP_ENABLED, vds/VDS_LUN_PLEX_FLAG, vdshwprv/VDS_LPF_LBN_REMAP_ENABLED, vdshwprv/VDS_LUN_PLEX_FLAG
req.header: vdshwprv.h
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
targetos: Windows
req.typenames: VDS_LUN_PLEX_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_LUN_PLEX_FLAG
 - vdshwprv/_VDS_LUN_PLEX_FLAG
 - VDS_LUN_PLEX_FLAG
 - vdshwprv/VDS_LUN_PLEX_FLAG
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
 - VDS_LUN_PLEX_FLAG
---

# VDS_LUN_PLEX_FLAG enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid flags for a LUN plex object.

## -enum-fields

### -field VDS_LPF_LBN_REMAP_ENABLED

If set, the provider remaps LUN extents to drive extents automatically. This flag corresponds to the <b>VDS_LF_LBN_REMAP_ENABLED</b> value of   the <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_flag">VDS_LUN_FLAG</a> enumeration.

## -remarks

This enumeration provides the value for the <b>ulFlags</b> member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_lun_plex_prop">VDS_LUN_PLEX_PROP</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_PLEX_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_PLEX_FLAG</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_lun_flag">VDS_LUN_FLAG</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_lun_plex_prop">VDS_LUN_PLEX_PROP</a>
