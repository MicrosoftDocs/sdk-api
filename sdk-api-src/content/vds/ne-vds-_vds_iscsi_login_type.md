---
UID: NE:vds._VDS_ISCSI_LOGIN_TYPE
title: "_VDS_ISCSI_LOGIN_TYPE"
author: windows-sdk-content
description: Defines the set of valid types for logging into an iSCSI target.
old-location: base\vds_iscsi_login_type.htm
tech.root: VDS
ms.assetid: d40db9ab-6fa5-4efb-83e8-ce1dce5fe0c2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: VDS_ILT_BOOT, VDS_ILT_MANUAL, VDS_ILT_PERSISTENT, VDS_ISCSI_LOGIN_TYPE, VDS_ISCSI_LOGIN_TYPE enumeration [VDS], _VDS_ISCSI_LOGIN_TYPE, base.vds_iscsi_login_type, vds/VDS_ILT_BOOT, vds/VDS_ILT_MANUAL, vds/VDS_ILT_PERSISTENT, vds/VDS_ISCSI_LOGIN_TYPE, vdshwprv/VDS_ILT_BOOT, vdshwprv/VDS_ILT_MANUAL, vdshwprv/VDS_ILT_PERSISTENT, vdshwprv/VDS_ISCSI_LOGIN_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_ISCSI_LOGIN_TYPE
product: Windows
targetos: Windows
req.typenames: VDS_ISCSI_LOGIN_TYPE
req.redist: VDS 1.1
---

# _VDS_ISCSI_LOGIN_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid types for logging into an iSCSI target.


## -enum-fields




### -field VDS_ILT_MANUAL

A manual, one-time login is performed.


### -field VDS_ILT_PERSISTENT

A persistent login is performed.


### -field VDS_ILT_BOOT

A persistent login is performed such that the target is present at startup.


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_ISCSI_LOGIN_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_ISCSI_LOGIN_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/74d6ddd0-1b78-446a-9bce-6816eb34a2b9">IVdsIscsiInitiatorAdapter::LoginToTarget</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>
 

 

