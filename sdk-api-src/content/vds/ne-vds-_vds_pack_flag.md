---
UID: NE:vds._VDS_PACK_FLAG
title: "_VDS_PACK_FLAG"
author: windows-driver-content
description: Defines the set of valid flags for a pack object.
old-location: base\vds_pack_flag.htm
old-project: VDS
ms.assetid: 65b7e65d-5d20-49ff-af35-bd3529f5c858
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: VDS_PACK_FLAG, VDS_PACK_FLAG enumeration [VDS], VDS_PKF_CORRUPTED, VDS_PKF_FOREIGN, VDS_PKF_NOQUORUM, VDS_PKF_ONLINE_ERROR, VDS_PKF_POLICY, _VDS_PACK_FLAG, base.vds_pack_flag, vds/VDS_PACK_FLAG, vds/VDS_PKF_CORRUPTED, vds/VDS_PKF_FOREIGN, vds/VDS_PKF_NOQUORUM, vds/VDS_PKF_ONLINE_ERROR, vds/VDS_PKF_POLICY
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VDS_PACK_FLAG
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
api_name:
-	VDS_PACK_FLAG
product: Windows
targetos: Windows
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
req.product: Windows UI
---

# _VDS_PACK_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid flags for a  pack object.


## -enum-fields




### -field VDS_PKF_FOREIGN

If set, an external pack is eligible for online status.


### -field VDS_PKF_NOQUORUM

If  set, a dynamic pack lacks the required quorum. A quorum is the minimum number of disks in a dynamic pack (n/2 + 1) required to enable online status. This flag prevents the caller from granting online status to the same pack on multiple computers.


### -field VDS_PKF_POLICY

If set, the pack policy prevents online eligibility.  This flag applies exclusively to packs managed by  the Windows Server 2003 version of VDS, which allows only one pack at a time to maintain online status.


### -field VDS_PKF_CORRUPTED

If set, a pack contains a disk with a corrupted database.


### -field VDS_PKF_ONLINE_ERROR

If set, a  pack with sufficient disk quorum failed to achieve online status due to an error.


## -remarks



Pack flags apply to packs managed by the dynamic provider only. The provider sets these flags on offline packs to report the reason for the offline status.

This enumeration provides the values for the <i>ulFlags</i> member of the <a href="https://msdn.microsoft.com/5d04bf6c-fda2-4b95-a8bb-907e64267f30">VDS_PACK_PROP</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PACK_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PACK_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/5d04bf6c-fda2-4b95-a8bb-907e64267f30">VDS_PACK_PROP</a>
 

 

