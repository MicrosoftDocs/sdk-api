---
UID: NE:vdshwprv._VDS_ISCSI_LOGIN_FLAG
title: VDS_ISCSI_LOGIN_FLAG (vdshwprv.h)
description: Defines the set of valid flags for specifying iSCSI target login options.
helpviewer_keywords: ["VDS_ILF_MULTIPATH_ENABLED","VDS_ILF_REQUIRE_IPSEC","VDS_ISCSI_LOGIN_FLAG","VDS_ISCSI_LOGIN_FLAG enumeration [VDS]","base.vds_iscsi_login_flag","vds/VDS_ILF_MULTIPATH_ENABLED","vds/VDS_ILF_REQUIRE_IPSEC","vds/VDS_ISCSI_LOGIN_FLAG","vdshwprv/VDS_ILF_MULTIPATH_ENABLED","vdshwprv/VDS_ILF_REQUIRE_IPSEC","vdshwprv/VDS_ISCSI_LOGIN_FLAG"]
old-location: base\vds_iscsi_login_flag.htm
tech.root: base
ms.assetid: c315f5cc-2b15-4185-8d22-7114950273e7
ms.date: 12/05/2018
ms.keywords: VDS_ILF_MULTIPATH_ENABLED, VDS_ILF_REQUIRE_IPSEC, VDS_ISCSI_LOGIN_FLAG, VDS_ISCSI_LOGIN_FLAG enumeration [VDS], base.vds_iscsi_login_flag, vds/VDS_ILF_MULTIPATH_ENABLED, vds/VDS_ILF_REQUIRE_IPSEC, vds/VDS_ISCSI_LOGIN_FLAG, vdshwprv/VDS_ILF_MULTIPATH_ENABLED, vdshwprv/VDS_ILF_REQUIRE_IPSEC, vdshwprv/VDS_ISCSI_LOGIN_FLAG
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: VDS_ISCSI_LOGIN_FLAG
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_ISCSI_LOGIN_FLAG
 - vdshwprv/_VDS_ISCSI_LOGIN_FLAG
 - VDS_ISCSI_LOGIN_FLAG
 - vdshwprv/VDS_ISCSI_LOGIN_FLAG
dev_langs:
 - c++
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
---

# VDS_ISCSI_LOGIN_FLAG enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid flags for specifying iSCSI target login options.

## -enum-fields

### -field VDS_ILF_REQUIRE_IPSEC:0x1

Reserved for future use.

### -field VDS_ILF_MULTIPATH_ENABLED:0x2

If this flag is set, the login is allowed to proceed and create a new login session even if there is already a login session to the target.
      

<div class="alert"><b>Note</b>  Multipathing software must be present or else data corruption may occur.</div>
<div> </div>

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_ISCSI_LOGIN_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_ISCSI_LOGIN_FLAG</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatoradapter-logintotarget">IVdsIscsiInitiatorAdapter::LoginToTarget</a>



<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>
