---
UID: NE:vdshwprv._VDS_INTERCONNECT_FLAG
title: "_VDS_INTERCONNECT_FLAG"
author: windows-sdk-content
description: Defines the set of interconnect types that subsystems can support.
old-location: base\vds_interconnect_flag.htm
tech.root: VDS
ms.assetid: ada895cb-1ff0-43df-8cd5-8ebc70cb97e2
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PVDS_INTERCONNECT_FLAG, VDS_INTERCONNECT_FLAG, VDS_INTERCONNECT_FLAG enumeration, VDS_ITF_FIBRE_CHANNEL, VDS_ITF_ISCSI, VDS_ITF_PCI_RAID, VDS_ITF_SAS, _VDS_INTERCONNECT_FLAG, base.vds_interconnect_flag, vds/VDS_INTERCONNECT_FLAG, vds/VDS_ITF_FIBRE_CHANNEL, vds/VDS_ITF_ISCSI, vds/VDS_ITF_PCI_RAID, vds/VDS_ITF_SAS, vdshwprv/VDS_INTERCONNECT_FLAG, vdshwprv/VDS_ITF_FIBRE_CHANNEL, vdshwprv/VDS_ITF_ISCSI, vdshwprv/VDS_ITF_PCI_RAID, vdshwprv/VDS_ITF_SAS"
ms.prod: windows
ms.technology: windows-sdk
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
---

# _VDS_INTERCONNECT_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

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




<a href="https://msdn.microsoft.com/5e8e69b4-023d-49f7-a363-bae1ae9536ac">IVdsSubSystemInterconnect::GetSupportedInterconnects</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/b16cc14b-4aef-43ec-9232-a95de06f1194">VDS_HWPROVIDER_TYPE</a>
 

 

