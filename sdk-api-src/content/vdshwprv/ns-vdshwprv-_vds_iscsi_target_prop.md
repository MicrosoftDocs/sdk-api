---
UID: NS:vdshwprv._VDS_ISCSI_TARGET_PROP
title: "_VDS_ISCSI_TARGET_PROP"
author: windows-sdk-content
description: Defines the properties of an iSCSI target.
old-location: base\vds_iscsi_target_prop.htm
old-project: VDS
ms.assetid: ca92c9e8-4d15-4b3c-8420-3eac18a7c2f5
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PVDS_ISCSI_TARGET_PROP, VDS_ISCSI_TARGET_PROP, VDS_ISCSI_TARGET_PROP structure [VDS], _VDS_ISCSI_TARGET_PROP, base.vds_iscsi_target_prop, vds/VDS_ISCSI_TARGET_PROP, vdshwprv/VDS_ISCSI_TARGET_PROP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: VDS_ISCSI_TARGET_PROP, *PVDS_ISCSI_TARGET_PROP
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Vds.h
-	VdsHwPrv.h
api_name:
-	VDS_ISCSI_TARGET_PROP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_ISCSI_TARGET_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of an iSCSI target.


## -struct-fields




### -field id

The <b>VDS_OBJECT_ID</b> of the target.


### -field pwszIscsiName

A null-terminated, human-readable string that is the iSCSI name of the target.


### -field pwszFriendlyName

A null-terminated, human-readable string that is the friendly name of the target. This corresponds to the 
     iSCSI alias.


### -field bChapEnabled

If <b>TRUE</b>, a CHAP shared secret is required to login to this target.


## -see-also




<a href="https://msdn.microsoft.com/db48ec8e-aae1-4b88-9942-6a23de2cfe25">IVdsIscsiTarget::GetProperties</a>
 

 

