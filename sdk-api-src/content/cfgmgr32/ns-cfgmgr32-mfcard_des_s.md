---
UID: NS:cfgmgr32.MfCard_Des_s
title: MfCard_Des_s
author: windows-sdk-content
description: The MFCARD_DES structure is used for specifying either a resource list or a resource requirements list that describes resource usage by one of the hardware functions provided by an instance of a multifunction device.
old-location: devinst\mfcard_des.htm
tech.root: devinst
ms.assetid: 75a6857c-d5b7-4bb6-8035-e6317d4ea146
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: "*PMFCARD_DES, MFCARD_DES, MFCARD_DES structure [Device and Driver Installation], MfCard_Des_s, PMFCARD_DES, PMFCARD_DES structure pointer [Device and Driver Installation], cfgmgr32/MFCARD_DES, cfgmgr32/PMFCARD_DES, cfgmgrst_aea737e9-53c7-41dd-b4d3-80f29442358c.xml, devinst.mfcard_des"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cfgmgr32.h
api_name:
 - MFCARD_DES
product: Windows
targetos: Windows
req.typenames: MFCARD_DES, *PMFCARD_DES
req.redist: 
---

# MfCard_Des_s structure


## -description


The MFCARD_DES structure is used for specifying either a resource list or a resource requirements list that describes resource usage by <i>one</i> of the hardware functions provided by an instance of a multifunction device. For more information about resource lists and resource requirements lists, see <a href="https://msdn.microsoft.com/c7a6997b-34f9-4dd9-b384-2321a8b5ce54">Hardware Resources</a>.


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

Zero-based index indicating the <a href="https://msdn.microsoft.com/d18a1f92-b76c-4240-9a0e-7474c258436c">IO_RESOURCE</a> structure that describes the I/O resources for the hardware function being described by this MFCARD_DES structure.


### -field PMF_Reserved

<i>Not used.</i>


### -field PMF_ConfigRegisterBase

Offset from the beginning of the card's attribute memory space to the base configuration register address.


## -see-also




<a href="https://msdn.microsoft.com/d18a1f92-b76c-4240-9a0e-7474c258436c">IO_RESOURCE</a>
 

 

