---
UID: NS:lmaccess._NET_VALIDATE_PASSWORD_HASH
title: NET_VALIDATE_PASSWORD_HASH (lmaccess.h)
description: The NET_VALIDATE_PASSWORD_HASH structure contains a password hash.
helpviewer_keywords: ["*PNET_VALIDATE_PASSWORD_HASH","NET_VALIDATE_PASSWORD_HASH","NET_VALIDATE_PASSWORD_HASH structure [Network Management]","PNET_VALIDATE_PASSWORD_HASH","PNET_VALIDATE_PASSWORD_HASH structure pointer [Network Management]","lmaccess/NET_VALIDATE_PASSWORD_HASH","lmaccess/PNET_VALIDATE_PASSWORD_HASH","netmgmt.net_validate_password_hash"]
old-location: netmgmt\net_validate_password_hash.htm
tech.root: NetMgmt
ms.assetid: 884e5b8c-1288-454e-862d-323d79123356
ms.date: 12/05/2018
ms.keywords: '*PNET_VALIDATE_PASSWORD_HASH, NET_VALIDATE_PASSWORD_HASH, NET_VALIDATE_PASSWORD_HASH structure [Network Management], PNET_VALIDATE_PASSWORD_HASH, PNET_VALIDATE_PASSWORD_HASH structure pointer [Network Management], lmaccess/NET_VALIDATE_PASSWORD_HASH, lmaccess/PNET_VALIDATE_PASSWORD_HASH, netmgmt.net_validate_password_hash'
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NET_VALIDATE_PASSWORD_HASH, *PNET_VALIDATE_PASSWORD_HASH
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_VALIDATE_PASSWORD_HASH
 - lmaccess/_NET_VALIDATE_PASSWORD_HASH
 - PNET_VALIDATE_PASSWORD_HASH
 - lmaccess/PNET_VALIDATE_PASSWORD_HASH
 - NET_VALIDATE_PASSWORD_HASH
 - lmaccess/NET_VALIDATE_PASSWORD_HASH
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmaccess.h
api_name:
 - NET_VALIDATE_PASSWORD_HASH
---

# NET_VALIDATE_PASSWORD_HASH structure


## -description

The <b>NET_VALIDATE_PASSWORD_HASH</b> structure contains a password hash.

## -struct-fields

### -field Length

Specifies the length of this structure.

### -field Hash

Password hash.

## -remarks

The <a href="/windows/win32/api/lmaccess/ns-lmaccess-net_validate_password_change_input_arg">NET_VALIDATE_PASSWORD_RESET_INPUT_ARG</a> and <a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_password_change_input_arg">NET_VALIDATE_PASSWORD_CHANGE_INPUT_ARG</a> structures contain a <b>NET_VALIDATE_PASSWORD_HASH</b> structure. The <a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_persisted_fields">NET_VALIDATE_PERSISTED_FIELDS</a> structure contains a pointer to this structure.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>