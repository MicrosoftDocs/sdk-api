---
UID: NS:vdshwprv._VDS_PROVIDER_PROP
title: VDS_PROVIDER_PROP (vdshwprv.h)
description: The VDS_PROVIDER_PROP structure (vdshwprv.h) defines the properties of a provider object.
helpviewer_keywords: ["VDS_PROVIDER_PROP","VDS_PROVIDER_PROP structure [VDS]","base.vds_provider_prop","vds/_VDS_PROVIDER_PROP","vdshwprv/_VDS_PROVIDER_PROP"]
old-location: base\vds_provider_prop.htm
tech.root: base
ms.assetid: f41fc908-3720-4dfb-a5d3-bb1459fb7e5d
ms.date: 08/09/2022
ms.keywords: VDS_PROVIDER_PROP, VDS_PROVIDER_PROP structure [VDS], base.vds_provider_prop, vds/_VDS_PROVIDER_PROP, vdshwprv/_VDS_PROVIDER_PROP
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
req.typenames: VDS_PROVIDER_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PROVIDER_PROP
 - vdshwprv/_VDS_PROVIDER_PROP
 - VDS_PROVIDER_PROP
 - vdshwprv/VDS_PROVIDER_PROP
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
 - VDS_PROVIDER_PROP
---

# VDS_PROVIDER_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
   properties of a <a href="/windows/desktop/VDS/provider-object">provider object</a>.

## -struct-fields

### -field id

The GUID of the provider object.

### -field pwszName

A string representing the name of the provider.

### -field guidVersionId

The version-specific GUID of the provider.

### -field pwszVersion

A string representing the version of the provider.

### -field type

The provider types enumerated by 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_provider_type">VDS_PROVIDER_TYPE</a>.

### -field ulFlags

The provider flags enumerated by 
      <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_provider_flag">VDS_PROVIDER_FLAG</a>.

### -field ulStripeSizeFlags

The size of a stripe to be used across multiple disks managed by a software provider. A stripe size must be 
      a power of 2. Each bit in the 32-bit integer represents a size, in bytes. For example, if the <i>n</i>th bit is set, then 
      VDS supports stripe size of 2^<i>n</i>. Thus, bits 0 through 31 can specify 2^0 through 2^31.

The basic provider sets this value to zero. The dynamic stripe size can be any power of 2 ranging from 512 
      to 1MB.
     

<b>Windows Server 2003:  </b>The dynamic provider sets this value to 64k.

### -field sRebuildPriority

The rebuild priority used by software providers to specify the regeneration order when a mirrored or 
      striped with parity (RAID-5) volume requires rebuilding. Priority levels are 0 (lowest priority) to 15 (highest priority). VDS propagates the 
      priority to all new volumes created by the provider. Thus, all volumes managed by a provider have the same 
      rebuild priority.

This member does not apply to the basic provider and is zero for the dynamic provider.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsprovider-getproperties">IVdsProvider::GetProperties</a> method 
    returns this structure to report the property details of a provider object.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsprovider-getproperties">IVdsProvider::GetProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_provider_flag">VDS_PROVIDER_FLAG</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_provider_type">VDS_PROVIDER_TYPE</a>
