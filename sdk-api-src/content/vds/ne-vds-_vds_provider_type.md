---
UID: NE:vds._VDS_PROVIDER_TYPE
title: "_VDS_PROVIDER_TYPE"
author: windows-sdk-content
description: Defines the set of valid types for a provider.
old-location: base\vds_provider_type.htm
old-project: VDS
ms.assetid: a794e054-1389-4b54-9ad3-eb32b9dd0a5b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: VDS_PROVIDER_TYPE, VDS_PROVIDER_TYPE enumeration [VDS], VDS_PT_HARDWARE, VDS_PT_MAX, VDS_PT_SOFTWARE, VDS_PT_UNKNOWN, VDS_PT_VIRTUALDISK, _VDS_PROVIDER_TYPE, base.vds_provider_type, vds/VDS_PROVIDER_TYPE, vds/VDS_PT_HARDWARE, vds/VDS_PT_MAX, vds/VDS_PT_SOFTWARE, vds/VDS_PT_UNKNOWN, vds/VDS_PT_VIRTUALDISK, vdshwprv/VDS_PROVIDER_TYPE, vdshwprv/VDS_PT_HARDWARE, vdshwprv/VDS_PT_MAX, vdshwprv/VDS_PT_SOFTWARE, vdshwprv/VDS_PT_UNKNOWN, vdshwprv/VDS_PT_VIRTUALDISK
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vds.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VDS_PROVIDER_TYPE
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
product: Windows
targetos: Windows
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
req.product: Windows UI
---

# _VDS_PROVIDER_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set 
   of valid types for a provider.


## -enum-fields




### -field VDS_PT_UNKNOWN

The provider type is unknown.


### -field VDS_PT_SOFTWARE

The provider is a software provider.


### -field VDS_PT_HARDWARE

The provider is a hardware provider.


### -field VDS_PT_VIRTUALDISK

The provider is a virtual disk provider.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


### -field VDS_PT_MAX

This value is reserved for system use.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


## -remarks



The <a href="https://msdn.microsoft.com/f41fc908-3720-4dfb-a5d3-bb1459fb7e5d">VDS_PROVIDER_PROP</a> structure includes a <b>VDS_PROVIDER_TYPE</b> 
    value as a member to report the provider type. The 
    <a href="https://msdn.microsoft.com/bb6e0037-7f44-418d-897c-12bf15224841">IVdsAdmin::RegisterProvider</a> method passes 
    a <b>VDS_PROVIDER_TYPE</b> value as an argument to indicate the provider type during registration with VDS.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PROVIDER_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PROVIDER_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/f41fc908-3720-4dfb-a5d3-bb1459fb7e5d">VDS_PROVIDER_PROP</a>
 

 

