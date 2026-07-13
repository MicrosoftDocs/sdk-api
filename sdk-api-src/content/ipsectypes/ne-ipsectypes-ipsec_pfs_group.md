---
UID: NE:ipsectypes.IPSEC_PFS_GROUP_
title: IPSEC_PFS_GROUP (ipsectypes.h)
description: Specifies the Diffie Hellman algorithm that should be used for Quick Mode PFS (Perfect Forward Secrecy).
helpviewer_keywords: ["IPSEC_PFS_1","IPSEC_PFS_14","IPSEC_PFS_2","IPSEC_PFS_2048","IPSEC_PFS_24","IPSEC_PFS_ECP_256","IPSEC_PFS_ECP_384","IPSEC_PFS_GROUP","IPSEC_PFS_GROUP enumeration [Filtering]","IPSEC_PFS_MAX","IPSEC_PFS_MM","IPSEC_PFS_NONE","fwp.ipsec_pfs_group_enum","ipsectypes/IPSEC_PFS_1","ipsectypes/IPSEC_PFS_14","ipsectypes/IPSEC_PFS_2","ipsectypes/IPSEC_PFS_2048","ipsectypes/IPSEC_PFS_24","ipsectypes/IPSEC_PFS_ECP_256","ipsectypes/IPSEC_PFS_ECP_384","ipsectypes/IPSEC_PFS_GROUP","ipsectypes/IPSEC_PFS_MAX","ipsectypes/IPSEC_PFS_MM","ipsectypes/IPSEC_PFS_NONE"]
old-location: fwp\ipsec_pfs_group_enum.htm
tech.root: fwp
ms.assetid: 0f0ea028-859b-42ca-a4e3-fe23f0836883
ms.date: 12/05/2018
ms.keywords: IPSEC_PFS_1, IPSEC_PFS_14, IPSEC_PFS_2, IPSEC_PFS_2048, IPSEC_PFS_24, IPSEC_PFS_ECP_256, IPSEC_PFS_ECP_384, IPSEC_PFS_GROUP, IPSEC_PFS_GROUP enumeration [Filtering], IPSEC_PFS_MAX, IPSEC_PFS_MM, IPSEC_PFS_NONE, fwp.ipsec_pfs_group_enum, ipsectypes/IPSEC_PFS_1, ipsectypes/IPSEC_PFS_14, ipsectypes/IPSEC_PFS_2, ipsectypes/IPSEC_PFS_2048, ipsectypes/IPSEC_PFS_24, ipsectypes/IPSEC_PFS_ECP_256, ipsectypes/IPSEC_PFS_ECP_384, ipsectypes/IPSEC_PFS_GROUP, ipsectypes/IPSEC_PFS_MAX, ipsectypes/IPSEC_PFS_MM, ipsectypes/IPSEC_PFS_NONE
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IPSEC_PFS_GROUP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPSEC_PFS_GROUP_
 - ipsectypes/IPSEC_PFS_GROUP_
 - IPSEC_PFS_GROUP
 - ipsectypes/IPSEC_PFS_GROUP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_PFS_GROUP
---

# IPSEC_PFS_GROUP enumeration


## -description

The <b>IPSEC_PFS_GROUP</b> enumerated type specifies the Diffie Hellman algorithm that should be used for 
Quick Mode PFS (Perfect Forward Secrecy).

## -enum-fields

### -field IPSEC_PFS_NONE:0

Specifies no Quick Mode PFS.

### -field IPSEC_PFS_1

Specifies Diffie Hellman group 1.

### -field IPSEC_PFS_2

Specifies Diffie Hellman group 2.

### -field IPSEC_PFS_2048

Specifies Diffie Hellman group 14.

### -field IPSEC_PFS_14

Specifies Diffie Hellman group 14.

<div class="alert"><b>Note</b>  This group was called Diffie Hellman group 2048 when it was introduced.  The name has since been changed to match standard terminology.</div>
<div> </div>
<div class="alert"><b>Note</b>  Available only for Windows 8 and Windows Server 2012. </div>
<div> </div>

### -field IPSEC_PFS_ECP_256

Specifies Diffie Hellman ECP group 256.

### -field IPSEC_PFS_ECP_384

Specifies Diffie Hellman ECP group 384.

### -field IPSEC_PFS_MM

Use the same Diffie Hellman as the main mode that contains this quick mode.

### -field IPSEC_PFS_24

Specifies Diffie Hellman group 24.

<div class="alert"><b>Note</b>  Available only for Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field IPSEC_PFS_MAX

Maximum value for testing only.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">WFP Enumerated Types</a>
