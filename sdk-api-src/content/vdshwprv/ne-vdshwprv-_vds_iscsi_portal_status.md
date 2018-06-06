---
UID: NE:vdshwprv._VDS_ISCSI_PORTAL_STATUS
title: "_VDS_ISCSI_PORTAL_STATUS"
author: windows-sdk-content
description: Defines the set of valid status values for an iSCSI portal.
old-location: base\vds_iscsi_portal_status.htm
old-project: VDS
ms.assetid: ae39dfb8-6519-4307-8038-3af670553f51
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: VDS_IPS_FAILED, VDS_IPS_NOT_READY, VDS_IPS_OFFLINE, VDS_IPS_ONLINE, VDS_IPS_UNKNOWN, VDS_ISCSI_PORTAL_STATUS, VDS_ISCSI_PORTAL_STATUS enumeration [VDS], _VDS_ISCSI_PORTAL_STATUS, base.vds_iscsi_portal_status, vds/VDS_IPS_FAILED, vds/VDS_IPS_NOT_READY, vds/VDS_IPS_OFFLINE, vds/VDS_IPS_ONLINE, vds/VDS_IPS_UNKNOWN, vds/VDS_ISCSI_PORTAL_STATUS, vdshwprv/VDS_IPS_FAILED, vdshwprv/VDS_IPS_NOT_READY, vdshwprv/VDS_IPS_OFFLINE, vdshwprv/VDS_IPS_ONLINE, vdshwprv/VDS_IPS_UNKNOWN, vdshwprv/VDS_ISCSI_PORTAL_STATUS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vdshwprv.h
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
tech.root: 
req.typenames: VDS_ISCSI_PORTAL_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_ISCSI_PORTAL_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_ISCSI_PORTAL_STATUS enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid status values for an iSCSI portal.


## -enum-fields




### -field VDS_IPS_UNKNOWN

The status is unknown.


### -field VDS_IPS_ONLINE

The portal is available.


### -field VDS_IPS_NOT_READY

The portal is busy.


### -field VDS_IPS_OFFLINE

The portal is unavailable.


### -field VDS_IPS_FAILED

The portal has failed.


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_ISCSI_PORTAL_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_ISCSI_PORTAL_STATUS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6c63fa36-bccb-4731-999a-c6f8b565b38f">IVdsIscsiPortal::SetStatus</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/da2d19ca-88a8-4a6a-bbe7-98a9d8af5b1b">VDS_ISCSI_PORTAL_PROP</a>
 

 

