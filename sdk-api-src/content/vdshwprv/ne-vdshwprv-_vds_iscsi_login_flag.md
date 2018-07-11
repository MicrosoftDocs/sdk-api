---
UID: NE:vdshwprv._VDS_ISCSI_LOGIN_FLAG
title: "_VDS_ISCSI_LOGIN_FLAG"
author: windows-sdk-content
description: Defines the set of valid flags for specifying iSCSI target login options.
old-location: base\vds_iscsi_login_flag.htm
old-project: vds
ms.assetid: c315f5cc-2b15-4185-8d22-7114950273e7
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: VDS_ILF_MULTIPATH_ENABLED, VDS_ILF_REQUIRE_IPSEC, VDS_ISCSI_LOGIN_FLAG, VDS_ISCSI_LOGIN_FLAG enumeration [VDS], _VDS_ISCSI_LOGIN_FLAG, base.vds_iscsi_login_flag, vds/VDS_ILF_MULTIPATH_ENABLED, vds/VDS_ILF_REQUIRE_IPSEC, vds/VDS_ISCSI_LOGIN_FLAG, vdshwprv/VDS_ILF_MULTIPATH_ENABLED, vdshwprv/VDS_ILF_REQUIRE_IPSEC, vdshwprv/VDS_ISCSI_LOGIN_FLAG
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
req.typenames: VDS_ISCSI_LOGIN_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_ISCSI_LOGIN_FLAG
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_ISCSI_LOGIN_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid flags for specifying iSCSI target login options.
   


## -enum-fields




### -field VDS_ILF_REQUIRE_IPSEC

Reserved for future use.
      


### -field VDS_ILF_MULTIPATH_ENABLED

If this flag is set, the login is allowed to proceed and create a new login session even if there is already a login session to the target.
      

<div class="alert"><b>Note</b>  Multipathing software must be present or else data corruption may occur.</div>
<div> </div>

## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_ISCSI_LOGIN_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_ISCSI_LOGIN_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/74d6ddd0-1b78-446a-9bce-6816eb34a2b9">IVdsIscsiInitiatorAdapter::LoginToTarget</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>
 

 

