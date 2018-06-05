---
UID: NE:vds._VDS_PARTITION_FLAG
title: "_VDS_PARTITION_FLAG"
author: windows-sdk-content
description: Defines a set of valid flags for a partition.
old-location: base\vds_partition_flag.htm
old-project: VDS
ms.assetid: d6ac5769-d0bc-4a4e-93c0-e9c83303ec4c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: VDS_PARTITION_FLAG, VDS_PARTITION_FLAG enumeration [VDS], VDS_PTF_SYSTEM, _VDS_PARTITION_FLAG, base.vds_partition_flag, vds/VDS_PARTITION_FLAG, vds/VDS_PTF_SYSTEM
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vds.h
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
tech.root: 
req.typenames: VDS_PARTITION_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
api_name:
-	VDS_PARTITION_FLAG
product: Windows
targetos: Windows
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
req.product: Windows UI
---

# _VDS_PARTITION_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines a set of valid flags for a partition.


## -enum-fields




### -field VDS_PTF_SYSTEM

If set, the partition is a system partition.


## -remarks




        This enumeration provides the values for the <i>ulFlags</i> member of the <a href="https://msdn.microsoft.com/f1b465ad-f03b-4ce8-ae83-f8e93b7fa4c4">VDS_PARTITION_PROP</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PARTITION_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PARTITION_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/f1b465ad-f03b-4ce8-ae83-f8e93b7fa4c4">VDS_PARTITION_PROP</a>
 

 

