---
UID: NE:vdshwprv._VDS_LUN_PLEX_FLAG
title: VDS_LUN_PLEX_FLAG
author: windows-sdk-content
description: Defines the set of valid flags for a LUN plex object.
old-location: base\vds_lun_plex_flag.htm
tech.root: VDS
ms.assetid: 0258d87c-0270-449e-8e96-2c511c5f7242
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VDS_LPF_LBN_REMAP_ENABLED, VDS_LUN_PLEX_FLAG, VDS_LUN_PLEX_FLAG enumeration [VDS], base.vds_lun_plex_flag, vds/VDS_LPF_LBN_REMAP_ENABLED, vds/VDS_LUN_PLEX_FLAG, vdshwprv/VDS_LPF_LBN_REMAP_ENABLED, vdshwprv/VDS_LUN_PLEX_FLAG
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_LUN_PLEX_FLAG
product: Windows
targetos: Windows
req.typenames: VDS_LUN_PLEX_FLAG
req.redist: 
---

# VDS_LUN_PLEX_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid flags for a LUN plex object.


## -enum-fields




### -field VDS_LPF_LBN_REMAP_ENABLED

If set, the provider remaps LUN extents to drive extents automatically. This flag corresponds to the <b>VDS_LF_LBN_REMAP_ENABLED</b> value of   the <a href="https://msdn.microsoft.com/977ee10c-c91f-4510-bf00-6b7d4da6c1c0">VDS_LUN_FLAG</a> enumeration.


## -remarks



This enumeration provides the value for the <b>ulFlags</b> member of the <a href="https://msdn.microsoft.com/d79ce5a9-af5a-4691-b853-c18d4a4d04c7">VDS_LUN_PLEX_PROP</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_PLEX_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_PLEX_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/977ee10c-c91f-4510-bf00-6b7d4da6c1c0">VDS_LUN_FLAG</a>



<a href="https://msdn.microsoft.com/d79ce5a9-af5a-4691-b853-c18d4a4d04c7">VDS_LUN_PLEX_PROP</a>
 

 

