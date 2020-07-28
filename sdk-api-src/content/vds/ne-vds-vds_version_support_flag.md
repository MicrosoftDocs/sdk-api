---
UID: NE:vds._VDS_VERSION_SUPPORT_FLAG
title: VDS_VERSION_SUPPORT_FLAG (vds.h)
description: Indicate which versions of the VDS interfaces are supported.
helpviewer_keywords: ["VDS_VERSION_SUPPORT_FLAG","VDS_VERSION_SUPPORT_FLAG enumeration","VDS_VSF_1_0","VDS_VSF_1_1","VDS_VSF_2_0","VDS_VSF_2_1","VDS_VSF_3_0","base.vds_version_support_flag","vds/VDS_VERSION_SUPPORT_FLAG","vds/VDS_VSF_1_0","vds/VDS_VSF_1_1","vds/VDS_VSF_2_0","vds/VDS_VSF_2_1","vds/VDS_VSF_3_0","vdshwprv/VDS_VERSION_SUPPORT_FLAG","vdshwprv/VDS_VSF_1_0","vdshwprv/VDS_VSF_1_1","vdshwprv/VDS_VSF_2_0","vdshwprv/VDS_VSF_2_1","vdshwprv/VDS_VSF_3_0"]
old-location: base\vds_version_support_flag.htm
tech.root: base
ms.assetid: c145070f-587f-42d7-bde9-3bf0cdba8444
ms.date: 12/05/2018
ms.keywords: VDS_VERSION_SUPPORT_FLAG, VDS_VERSION_SUPPORT_FLAG enumeration, VDS_VSF_1_0, VDS_VSF_1_1, VDS_VSF_2_0, VDS_VSF_2_1, VDS_VSF_3_0, base.vds_version_support_flag, vds/VDS_VERSION_SUPPORT_FLAG, vds/VDS_VSF_1_0, vds/VDS_VSF_1_1, vds/VDS_VSF_2_0, vds/VDS_VSF_2_1, vds/VDS_VSF_3_0, vdshwprv/VDS_VERSION_SUPPORT_FLAG, vdshwprv/VDS_VSF_1_0, vdshwprv/VDS_VSF_1_1, vdshwprv/VDS_VSF_2_0, vdshwprv/VDS_VSF_2_1, vdshwprv/VDS_VSF_3_0
f1_keywords:
- vds/VDS_VERSION_SUPPORT_FLAG
dev_langs:
- c++
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
- VDS_VERSION_SUPPORT_FLAG
targetos: Windows
req.typenames: VDS_VERSION_SUPPORT_FLAG
req.redist: 
ms.custom: 19H1
---

# VDS_VERSION_SUPPORT_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Used to 
    indicate which versions of the VDS interfaces are supported.


## -enum-fields




### -field VDS_VSF_1_0

Indicates that the VDS 1.0 interfaces are supported. VDS 1.0 is supported on 
      Windows Server 2003 and later.


### -field VDS_VSF_1_1

Indicates that the VDS 1.1 interfaces are supported. VDS 1.1 is supported on 
      Windows Server 2003 R2 and later.


### -field VDS_VSF_2_0

Indicates that the VDS 2.0 interfaces are supported. VDS 2.0 is supported on Windows Vista and 
      later.
      

<b>Windows Server 2008, Windows Vista and Windows Server 2003 R2:  </b>This value is not supported.


### -field VDS_VSF_2_1

Indicates that the VDS 2.1 interfaces are supported. VDS 2.1 is supported on Windows Vista with SP1,  
      Windows Server 2008, and later.
      

<b>Windows Server 2008, Windows Vista and Windows Server 2003 R2:  </b>This value is not supported.


### -field VDS_VSF_3_0

Indicates that the VDS 3.0 interfaces are supported. VDS 3.0 is supported on Windows 7, 
      Windows Server 2008 R2, and later.
      

<b>Windows Server 2008, Windows Vista and Windows Server 2003 R2:  </b>This value is not supported.


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the 
    <b>VDS_VERSION_SUPPORT_FLAG</b> enumeration in future 
    Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized 
    <b>VDS_VERSION_SUPPORT_FLAG</b> enumeration 
    constant.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsprovidersupport-getversionsupport">IVdsProviderSupport::GetVersionSupport</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>
 

 

