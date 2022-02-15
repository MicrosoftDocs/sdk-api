---
UID: NE:vds._VDS_HBAPORT_SPEED_FLAG
title: VDS_HBAPORT_SPEED_FLAG (vds.h)
description: Defines the set of valid flags for determining the speeds supported by an HBA port.
helpviewer_keywords: ["VDS_HBAPORT_SPEED_FLAG","VDS_HBAPORT_SPEED_FLAG enumeration [VDS]","VDS_HSF_10GBIT","VDS_HSF_1GBIT","VDS_HSF_2GBIT","VDS_HSF_4GBIT","VDS_HSF_NOT_NEGOTIATED","VDS_HSF_UNKNOWN","base.vds_hbaport_speed_flag","vds/VDS_HBAPORT_SPEED_FLAG","vds/VDS_HSF_10GBIT","vds/VDS_HSF_1GBIT","vds/VDS_HSF_2GBIT","vds/VDS_HSF_4GBIT","vds/VDS_HSF_NOT_NEGOTIATED","vds/VDS_HSF_UNKNOWN","vdshwprv/VDS_HBAPORT_SPEED_FLAG","vdshwprv/VDS_HSF_10GBIT","vdshwprv/VDS_HSF_1GBIT","vdshwprv/VDS_HSF_2GBIT","vdshwprv/VDS_HSF_4GBIT","vdshwprv/VDS_HSF_NOT_NEGOTIATED","vdshwprv/VDS_HSF_UNKNOWN"]
old-location: base\vds_hbaport_speed_flag.htm
tech.root: base
ms.assetid: b44a51b5-7aca-4e95-88ec-60ff026c411f
ms.date: 12/05/2018
ms.keywords: VDS_HBAPORT_SPEED_FLAG, VDS_HBAPORT_SPEED_FLAG enumeration [VDS], VDS_HSF_10GBIT, VDS_HSF_1GBIT, VDS_HSF_2GBIT, VDS_HSF_4GBIT, VDS_HSF_NOT_NEGOTIATED, VDS_HSF_UNKNOWN, base.vds_hbaport_speed_flag, vds/VDS_HBAPORT_SPEED_FLAG, vds/VDS_HSF_10GBIT, vds/VDS_HSF_1GBIT, vds/VDS_HSF_2GBIT, vds/VDS_HSF_4GBIT, vds/VDS_HSF_NOT_NEGOTIATED, vds/VDS_HSF_UNKNOWN, vdshwprv/VDS_HBAPORT_SPEED_FLAG, vdshwprv/VDS_HSF_10GBIT, vdshwprv/VDS_HSF_1GBIT, vdshwprv/VDS_HSF_2GBIT, vdshwprv/VDS_HSF_4GBIT, vdshwprv/VDS_HSF_NOT_NEGOTIATED, vdshwprv/VDS_HSF_UNKNOWN
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
req.typenames: VDS_HBAPORT_SPEED_FLAG
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_HBAPORT_SPEED_FLAG
 - vds/_VDS_HBAPORT_SPEED_FLAG
 - VDS_HBAPORT_SPEED_FLAG
 - vds/VDS_HBAPORT_SPEED_FLAG
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
 - VDS_HBAPORT_SPEED_FLAG
---

# VDS_HBAPORT_SPEED_FLAG enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid flags for determining the speeds supported by an HBA port. 
    These values are used in the <b>ulPortSpeed</b> member of the 
    <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hbaport_prop">VDS_HBAPORT_PROP</a> structure.

## -enum-fields

### -field VDS_HSF_UNKNOWN:0

The HBA port speed is unknown. The transceiver is incapable of reporting.
      

HBA_PORTSPEED_UNKNOWN

### -field VDS_HSF_1GBIT:0x1

The HBA port supports a transfer rate of 1 gigabit per second.
      

HBA_PORTSPEED_1GBIT

### -field VDS_HSF_2GBIT:0x2

The HBA port supports a transfer rate of 2 gigabits per second.
      

HBA_PORTSPEED_2GBIT

### -field VDS_HSF_10GBIT:0x4

The HBA port supports a transfer rate of 10 gigabits per second.
      

HBA_PORTSPEED_10GBIT

### -field VDS_HSF_4GBIT:0x8

The HBA port supports a transfer rate of 4 gigabits per second.
      

HBA_PORTSPEED_4GBIT

### -field VDS_HSF_NOT_NEGOTIATED

The HBA port speed has not been established.
      

HBA_PORTSPEED_NOT_NEGOTIATED

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_HBAPORT_SPEED_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_HBAPORT_SPEED_FLAG</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_hbaport_prop">VDS_HBAPORT_PROP</a>
