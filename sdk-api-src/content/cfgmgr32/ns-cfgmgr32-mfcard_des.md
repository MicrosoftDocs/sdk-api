---
UID: NS:cfgmgr32.MfCard_Des_s
title: MFCARD_DES (cfgmgr32.h)
description: The MFCARD_DES structure is used for specifying either a resource list or a resource requirements list that describes resource usage by one of the hardware functions provided by an instance of a multifunction device.
helpviewer_keywords: ["*PMFCARD_DES","MFCARD_DES","MFCARD_DES structure [Device and Driver Installation]","PMFCARD_DES","PMFCARD_DES structure pointer [Device and Driver Installation]","cfgmgr32/MFCARD_DES","cfgmgr32/PMFCARD_DES","cfgmgrst_aea737e9-53c7-41dd-b4d3-80f29442358c.xml","devinst.mfcard_des"]
old-location: devinst\mfcard_des.htm
tech.root: devinst
ms.assetid: 75a6857c-d5b7-4bb6-8035-e6317d4ea146
ms.date: 12/05/2018
ms.keywords: '*PMFCARD_DES, MFCARD_DES, MFCARD_DES structure [Device and Driver Installation], PMFCARD_DES, PMFCARD_DES structure pointer [Device and Driver Installation], cfgmgr32/MFCARD_DES, cfgmgr32/PMFCARD_DES, cfgmgrst_aea737e9-53c7-41dd-b4d3-80f29442358c.xml, devinst.mfcard_des'
req.header: cfgmgr32.h
req.include-header: Cfgmgr32.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MFCARD_DES, *PMFCARD_DES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MfCard_Des_s
 - cfgmgr32/MfCard_Des_s
 - PMFCARD_DES
 - cfgmgr32/PMFCARD_DES
 - MFCARD_DES
 - cfgmgr32/MFCARD_DES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - MFCARD_DES
---

# MFCARD_DES structure


## -description

The MFCARD_DES structure is used for specifying either a resource list or a resource requirements list that describes resource usage by <i>one</i> of the hardware functions provided by an instance of a multifunction device. For more information about resource lists and resource requirements lists, see <a href="/windows-hardware/drivers/kernel/hardware-resources">Hardware Resources</a>.

## -struct-fields

### -field PMF_Count

Must be 1.

### -field PMF_Type

<i>Not used.</i>

### -field PMF_Flags

One bit flag is defined, as described in the following table.

<table>
<tr>
<th>Flag</th>
<th>Definition</th>
</tr>
<tr>
<td>
fPMF_AUDIO_ENABLE

</td>
<td>
If set, audio is enabled.

</td>
</tr>
</table>

### -field PMF_ConfigOptions

Contents of the 8-bit PCMCIA Configuration Option Register.

### -field PMF_IoResourceIndex

Zero-based index indicating the [IO_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_resource) structure that describes the I/O resources for the hardware function being described by this MFCARD_DES structure.

### -field PMF_Reserved

<i>Not used.</i>

### -field PMF_ConfigRegisterBase

Offset from the beginning of the card's attribute memory space to the base configuration register address.

## -see-also

[IO_RESOURCE](/windows/desktop/api/cfgmgr32/ns-cfgmgr32-io_resource)