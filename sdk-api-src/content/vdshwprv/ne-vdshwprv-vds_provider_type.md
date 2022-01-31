---
UID: NE:vdshwprv._VDS_PROVIDER_TYPE
title: VDS_PROVIDER_TYPE (vdshwprv.h)
description: Defines the set of valid types for a provider.
helpviewer_keywords: ["VDS_PROVIDER_TYPE","VDS_PROVIDER_TYPE enumeration [VDS]","VDS_PT_HARDWARE","VDS_PT_MAX","VDS_PT_SOFTWARE","VDS_PT_UNKNOWN","VDS_PT_VIRTUALDISK","base.vds_provider_type","vds/VDS_PROVIDER_TYPE","vds/VDS_PT_HARDWARE","vds/VDS_PT_MAX","vds/VDS_PT_SOFTWARE","vds/VDS_PT_UNKNOWN","vds/VDS_PT_VIRTUALDISK","vdshwprv/VDS_PROVIDER_TYPE","vdshwprv/VDS_PT_HARDWARE","vdshwprv/VDS_PT_MAX","vdshwprv/VDS_PT_SOFTWARE","vdshwprv/VDS_PT_UNKNOWN","vdshwprv/VDS_PT_VIRTUALDISK"]
old-location: base\vds_provider_type.htm
tech.root: base
ms.assetid: a794e054-1389-4b54-9ad3-eb32b9dd0a5b
ms.date: 12/05/2018
ms.keywords: VDS_PROVIDER_TYPE, VDS_PROVIDER_TYPE enumeration [VDS], VDS_PT_HARDWARE, VDS_PT_MAX, VDS_PT_SOFTWARE, VDS_PT_UNKNOWN, VDS_PT_VIRTUALDISK, base.vds_provider_type, vds/VDS_PROVIDER_TYPE, vds/VDS_PT_HARDWARE, vds/VDS_PT_MAX, vds/VDS_PT_SOFTWARE, vds/VDS_PT_UNKNOWN, vds/VDS_PT_VIRTUALDISK, vdshwprv/VDS_PROVIDER_TYPE, vdshwprv/VDS_PT_HARDWARE, vdshwprv/VDS_PT_MAX, vdshwprv/VDS_PT_SOFTWARE, vdshwprv/VDS_PT_UNKNOWN, vdshwprv/VDS_PT_VIRTUALDISK
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
req.typenames: VDS_PROVIDER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PROVIDER_TYPE
 - vdshwprv/_VDS_PROVIDER_TYPE
 - VDS_PROVIDER_TYPE
 - vdshwprv/VDS_PROVIDER_TYPE
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
 - VDS_PROVIDER_TYPE
---

# VDS_PROVIDER_TYPE enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set 
   of valid types for a provider.

## -enum-fields

### -field VDS_PT_UNKNOWN:0

The provider type is unknown.

### -field VDS_PT_SOFTWARE:1

The provider is a software provider.

### -field VDS_PT_HARDWARE:2

The provider is a hardware provider.

### -field VDS_PT_VIRTUALDISK:3

The provider is a virtual disk provider.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.

### -field VDS_PT_MAX:4

This value is reserved for system use.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_provider_prop">VDS_PROVIDER_PROP</a> structure includes a <b>VDS_PROVIDER_TYPE</b> 
    value as a member to report the provider type. The 
    <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsadmin-registerprovider">IVdsAdmin::RegisterProvider</a> method passes 
    a <b>VDS_PROVIDER_TYPE</b> value as an argument to indicate the provider type during registration with VDS.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PROVIDER_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PROVIDER_TYPE</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_provider_prop">VDS_PROVIDER_PROP</a>
