---
UID: NE:vdshwprv._VDS_INTERCONNECT_FLAG
title: VDS_INTERCONNECT_FLAG (vdshwprv.h)
author: windows-sdk-content
description: Defines the set of interconnect types that subsystems can support.
old-location: base\vds_interconnect_flag.htm
tech.root: VDS
ms.assetid: ada895cb-1ff0-43df-8cd5-8ebc70cb97e2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PVDS_INTERCONNECT_FLAG, VDS_INTERCONNECT_FLAG, VDS_INTERCONNECT_FLAG enumeration, VDS_ITF_FIBRE_CHANNEL, VDS_ITF_ISCSI, VDS_ITF_PCI_RAID, VDS_ITF_SAS, base.vds_interconnect_flag, vds/VDS_INTERCONNECT_FLAG, vds/VDS_ITF_FIBRE_CHANNEL, vds/VDS_ITF_ISCSI, vds/VDS_ITF_PCI_RAID, vds/VDS_ITF_SAS, vdshwprv/VDS_INTERCONNECT_FLAG, vdshwprv/VDS_ITF_FIBRE_CHANNEL, vdshwprv/VDS_ITF_ISCSI, vdshwprv/VDS_ITF_PCI_RAID, vdshwprv/VDS_ITF_SAS"
ms.topic: enum
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - VDS_INTERCONNECT_FLAG
product: Windows
targetos: Windows
req.typenames: VDS_INTERCONNECT_FLAG, *PVDS_INTERCONNECT_FLAG
req.redist: 
ms.custom: 19H1
---

# VDS_INTERCONNECT_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of interconnect types that subsystems can support.


## -enum-fields




### -field VDS_ITF_PCI_RAID

The subsystem supports a PCI RAID interconnect.


### -field VDS_ITF_FIBRE_CHANNEL

The subsystem supports a Fibre Channel interconnect.


### -field VDS_ITF_ISCSI

The subsystem supports an iSCSI interconnect.


### -field VDS_ITF_SAS

The subsystem supports a serial attached iSCSI (SAS) interconnect.


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_INTERCONNECT_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_INTERCONNECT_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsysteminterconnect-getsupportedinterconnects">IVdsSubSystemInterconnect::GetSupportedInterconnects</a>



<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vdshwprv/ne-vdshwprv-_vds_hwprovider_type">VDS_HWPROVIDER_TYPE</a>
 

 

