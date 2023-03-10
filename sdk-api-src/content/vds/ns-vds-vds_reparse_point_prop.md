---
UID: NS:vds.VDS_REPARSE_POINT_PROP
title: VDS_REPARSE_POINT_PROP (vds.h)
description: Defines the reparse-point properties of a volume object.
helpviewer_keywords: ["*PVDS_REPARSE_POINT_PROP","PVDS_REPARSE_POINT_PROP","PVDS_REPARSE_POINT_PROP structure pointer [VDS]","VDS_REPARSE_POINT_PROP","VDS_REPARSE_POINT_PROP structure [VDS]","base.vds_reparse_point_prop","vds/PVDS_REPARSE_POINT_PROP","vds/VDS_REPARSE_POINT_PROP"]
old-location: base\vds_reparse_point_prop.htm
tech.root: base
ms.assetid: 7e224f49-c51f-447e-bc0b-6af3843e01ae
ms.date: 12/05/2018
ms.keywords: '*PVDS_REPARSE_POINT_PROP, PVDS_REPARSE_POINT_PROP, PVDS_REPARSE_POINT_PROP structure pointer [VDS], VDS_REPARSE_POINT_PROP, VDS_REPARSE_POINT_PROP structure [VDS], base.vds_reparse_point_prop, vds/PVDS_REPARSE_POINT_PROP, vds/VDS_REPARSE_POINT_PROP'
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
targetos: Windows
req.typenames: VDS_REPARSE_POINT_PROP, *PVDS_REPARSE_POINT_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VDS_REPARSE_POINT_PROP
 - vds/VDS_REPARSE_POINT_PROP
 - PVDS_REPARSE_POINT_PROP
 - vds/PVDS_REPARSE_POINT_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_REPARSE_POINT_PROP
---

# VDS_REPARSE_POINT_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the reparse-point properties of a  <a href="/windows/desktop/VDS/volume-object">volume object</a>.

## -struct-fields

### -field SourceVolumeId

The GUID of the volume object that contains the reparse point.

### -field pwszPath

A string for a path without a drive letter. For example, "\mount".

## -remarks

The <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-queryreparsepoints">IVdsVolumeMF::QueryReparsePoints</a> method returns this structure to report the reparse-point properties of a <a href="/windows/desktop/VDS/volume-object">volume object</a>.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-queryreparsepoints">IVdsVolumeMF::QueryReparsePoints</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>