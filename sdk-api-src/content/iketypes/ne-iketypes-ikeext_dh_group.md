---
UID: NE:iketypes.IKEEXT_DH_GROUP_
title: IKEEXT_DH_GROUP (iketypes.h)
description: Specifies the type of Diffie Hellman group used for Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP) key generation.
helpviewer_keywords: ["IKEEXT_DH_ECP_256","IKEEXT_DH_ECP_384","IKEEXT_DH_GROUP","IKEEXT_DH_GROUP enumeration [Filtering]","IKEEXT_DH_GROUP_1","IKEEXT_DH_GROUP_14","IKEEXT_DH_GROUP_2","IKEEXT_DH_GROUP_2048","IKEEXT_DH_GROUP_24","IKEEXT_DH_GROUP_MAX","IKEEXT_DH_GROUP_NONE","fwp.ikeext_dh_group","iketypes/IKEEXT_DH_ECP_256","iketypes/IKEEXT_DH_ECP_384","iketypes/IKEEXT_DH_GROUP","iketypes/IKEEXT_DH_GROUP_1","iketypes/IKEEXT_DH_GROUP_14","iketypes/IKEEXT_DH_GROUP_2","iketypes/IKEEXT_DH_GROUP_2048","iketypes/IKEEXT_DH_GROUP_24","iketypes/IKEEXT_DH_GROUP_MAX","iketypes/IKEEXT_DH_GROUP_NONE"]
old-location: fwp\ikeext_dh_group.htm
tech.root: fwp
ms.assetid: ed90c404-f713-4a0d-9698-eece1bfb7dd7
ms.date: 12/05/2018
ms.keywords: IKEEXT_DH_ECP_256, IKEEXT_DH_ECP_384, IKEEXT_DH_GROUP, IKEEXT_DH_GROUP enumeration [Filtering], IKEEXT_DH_GROUP_1, IKEEXT_DH_GROUP_14, IKEEXT_DH_GROUP_2, IKEEXT_DH_GROUP_2048, IKEEXT_DH_GROUP_24, IKEEXT_DH_GROUP_MAX, IKEEXT_DH_GROUP_NONE, fwp.ikeext_dh_group, iketypes/IKEEXT_DH_ECP_256, iketypes/IKEEXT_DH_ECP_384, iketypes/IKEEXT_DH_GROUP, iketypes/IKEEXT_DH_GROUP_1, iketypes/IKEEXT_DH_GROUP_14, iketypes/IKEEXT_DH_GROUP_2, iketypes/IKEEXT_DH_GROUP_2048, iketypes/IKEEXT_DH_GROUP_24, iketypes/IKEEXT_DH_GROUP_MAX, iketypes/IKEEXT_DH_GROUP_NONE
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_DH_GROUP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_DH_GROUP_
 - iketypes/IKEEXT_DH_GROUP_
 - IKEEXT_DH_GROUP
 - iketypes/IKEEXT_DH_GROUP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_DH_GROUP
---

# IKEEXT_DH_GROUP enumeration


## -description

The <b>IKEEXT_DH_GROUP</b> enumerated type specifies the type of Diffie Hellman group used for Internet Key Exchange (IKE) and Authenticated Internet Protocol (AuthIP) key generation.

## -enum-fields

### -field IKEEXT_DH_GROUP_NONE:0

Specifies no Diffie Hellman group. Available only for AuthIP.

### -field IKEEXT_DH_GROUP_1

Specifies  Diffie Hellman group 1.

### -field IKEEXT_DH_GROUP_2

Specifies  Diffie Hellman group 2.

### -field IKEEXT_DH_GROUP_14

Specifies  Diffie Hellman group 14.

<div class="alert"><b>Note</b>  Available only for Windows 8 and Windows Server 2012. </div>
<div> </div>

### -field IKEEXT_DH_GROUP_2048

Specifies  Diffie Hellman group 14.

<div class="alert"><b>Note</b>  This group was called Diffie Hellman group 2048 when it was introduced.  The name has since been changed to match standard terminology.</div>
<div> </div>

### -field IKEEXT_DH_ECP_256

Specifies Diffie Hellman ECP group 256.

### -field IKEEXT_DH_ECP_384

Specifies Diffie Hellman ECP group 384.

### -field IKEEXT_DH_GROUP_24

Specifies  Diffie Hellman group 24.

<div class="alert"><b>Note</b>  Available only for Windows 8 and Windows Server 2012.</div>
<div> </div>

### -field IKEEXT_DH_GROUP_MAX

Maximum value for testing purposes.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
