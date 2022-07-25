---
UID: NE:vds._VDS_QUERY_PROVIDER_FLAG
title: VDS_QUERY_PROVIDER_FLAG (vds.h)
description: Defines the set of valid flags for provider query operations. Callers can query for hardware providers, software providers, or both.
helpviewer_keywords: ["VDS_QUERY_HARDWARE_PROVIDERS","VDS_QUERY_PROVIDER_FLAG","VDS_QUERY_PROVIDER_FLAG enumeration [VDS]","VDS_QUERY_SOFTWARE_PROVIDERS","VDS_QUERY_VIRTUALDISK_PROVIDERS","base.vds_query_provider_flag","vds/VDS_QUERY_HARDWARE_PROVIDERS","vds/VDS_QUERY_PROVIDER_FLAG","vds/VDS_QUERY_SOFTWARE_PROVIDERS","vds/VDS_QUERY_VIRTUALDISK_PROVIDERS","vdshwprv/VDS_QUERY_HARDWARE_PROVIDERS","vdshwprv/VDS_QUERY_PROVIDER_FLAG","vdshwprv/VDS_QUERY_SOFTWARE_PROVIDERS","vdshwprv/VDS_QUERY_VIRTUALDISK_PROVIDERS"]
old-location: base\vds_query_provider_flag.htm
tech.root: base
ms.assetid: 849b3cbc-a1ed-438a-8fda-ada096fb8375
ms.date: 12/05/2018
ms.keywords: VDS_QUERY_HARDWARE_PROVIDERS, VDS_QUERY_PROVIDER_FLAG, VDS_QUERY_PROVIDER_FLAG enumeration [VDS], VDS_QUERY_SOFTWARE_PROVIDERS, VDS_QUERY_VIRTUALDISK_PROVIDERS, base.vds_query_provider_flag, vds/VDS_QUERY_HARDWARE_PROVIDERS, vds/VDS_QUERY_PROVIDER_FLAG, vds/VDS_QUERY_SOFTWARE_PROVIDERS, vds/VDS_QUERY_VIRTUALDISK_PROVIDERS, vdshwprv/VDS_QUERY_HARDWARE_PROVIDERS, vdshwprv/VDS_QUERY_PROVIDER_FLAG, vdshwprv/VDS_QUERY_SOFTWARE_PROVIDERS, vdshwprv/VDS_QUERY_VIRTUALDISK_PROVIDERS
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
req.typenames: VDS_QUERY_PROVIDER_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_QUERY_PROVIDER_FLAG
 - vds/_VDS_QUERY_PROVIDER_FLAG
 - VDS_QUERY_PROVIDER_FLAG
 - vds/VDS_QUERY_PROVIDER_FLAG
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
 - VDS_QUERY_PROVIDER_FLAG
---

# VDS_QUERY_PROVIDER_FLAG enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid flags for provider query operations. Callers can query for hardware providers, software providers, or both.

## -enum-fields

### -field VDS_QUERY_SOFTWARE_PROVIDERS:0x1

If set, the operation queries for software providers.

### -field VDS_QUERY_HARDWARE_PROVIDERS:0x2

If set, the operation queries for hardware providers.

### -field VDS_QUERY_VIRTUALDISK_PROVIDERS:0x4

If set, the operation queries for virtual disk providers.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.

## -remarks

This enumeration provides the value for the <i>masks</i> parameter of the  <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-queryproviders">IVdsService::QueryProviders</a> method. You can specify more than  one value in the same query. For example, to query for software and hardware providers, specify both VDS_QUERY_SOFTWARE_PROVIDERS and VDS_QUERY_HARDWARE_PROVIDERS in the <i>masks</i> parameter.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_QUERY_PROVIDER_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_QUERY_PROVIDER_FLAG</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-queryproviders">IVdsService::QueryProviders</a>



<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>
