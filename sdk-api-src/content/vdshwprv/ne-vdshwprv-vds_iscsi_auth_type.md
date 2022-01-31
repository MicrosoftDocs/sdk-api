---
UID: NE:vdshwprv._VDS_ISCSI_AUTH_TYPE
title: VDS_ISCSI_AUTH_TYPE (vdshwprv.h)
description: Defines the set of valid types for authentication when logging into an iSCSI target.
helpviewer_keywords: ["VDS_IAT_CHAP","VDS_IAT_MUTUAL_CHAP","VDS_IAT_NONE","VDS_ISCSI_AUTH_TYPE","VDS_ISCSI_AUTH_TYPE enumeration [VDS]","base.vds_iscsi_auth_type","vds/VDS_IAT_CHAP","vds/VDS_IAT_MUTUAL_CHAP","vds/VDS_IAT_NONE","vds/VDS_ISCSI_AUTH_TYPE","vdshwprv/VDS_IAT_CHAP","vdshwprv/VDS_IAT_MUTUAL_CHAP","vdshwprv/VDS_IAT_NONE","vdshwprv/VDS_ISCSI_AUTH_TYPE"]
old-location: base\vds_iscsi_auth_type.htm
tech.root: base
ms.assetid: 7e445b10-552a-4a89-aee8-9699db79c5a3
ms.date: 12/05/2018
ms.keywords: VDS_IAT_CHAP, VDS_IAT_MUTUAL_CHAP, VDS_IAT_NONE, VDS_ISCSI_AUTH_TYPE, VDS_ISCSI_AUTH_TYPE enumeration [VDS], base.vds_iscsi_auth_type, vds/VDS_IAT_CHAP, vds/VDS_IAT_MUTUAL_CHAP, vds/VDS_IAT_NONE, vds/VDS_ISCSI_AUTH_TYPE, vdshwprv/VDS_IAT_CHAP, vdshwprv/VDS_IAT_MUTUAL_CHAP, vdshwprv/VDS_IAT_NONE, vdshwprv/VDS_ISCSI_AUTH_TYPE
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
req.typenames: VDS_ISCSI_AUTH_TYPE
req.redist: VDS 1.1
ms.custom: 19H1
f1_keywords:
 - _VDS_ISCSI_AUTH_TYPE
 - vdshwprv/_VDS_ISCSI_AUTH_TYPE
 - VDS_ISCSI_AUTH_TYPE
 - vdshwprv/VDS_ISCSI_AUTH_TYPE
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
 - VDS_ISCSI_AUTH_TYPE
---

# VDS_ISCSI_AUTH_TYPE enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid types for authentication when logging into an iSCSI target.

## -enum-fields

### -field VDS_IAT_NONE:0

No authentication is performed.

### -field VDS_IAT_CHAP:1

One-way CHAP authentication is performed (target authenticates initiator). The target CHAP secret must be 
     specified during login.

### -field VDS_IAT_MUTUAL_CHAP:2

Mutual CHAP authentication is performed (target authenticates initiator and initiator authenticates 
     target). The target CHAP secret must be specified and the initiator CHAP secret must also have been set.

## -remarks

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_ISCSI_AUTH_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_ISCSI_AUTH_TYPE</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsiscsiinitiatoradapter-logintotarget">IVdsIscsiInitiatorAdapter::LoginToTarget</a>
