---
UID: NS:lmaccess._NET_VALIDATE_AUTHENTICATION_INPUT_ARG
title: NET_VALIDATE_AUTHENTICATION_INPUT_ARG (lmaccess.h)
description: A client application passes the NET_VALIDATE_AUTHENTICATION_INPUT_ARG structure to the NetValidatePasswordPolicy function when the application requests an authentication validation.
helpviewer_keywords: ["*PNET_VALIDATE_AUTHENTICATION_INPUT_ARG","NET_VALIDATE_AUTHENTICATION_INPUT_ARG","NET_VALIDATE_AUTHENTICATION_INPUT_ARG structure [Network Management]","PNET_VALIDATE_AUTHENTICATION_INPUT_ARG","PNET_VALIDATE_AUTHENTICATION_INPUT_ARG structure pointer [Network Management]","lmaccess/NET_VALIDATE_AUTHENTICATION_INPUT_ARG","lmaccess/PNET_VALIDATE_AUTHENTICATION_INPUT_ARG","netmgmt.net_validate_authentication_input_arg"]
old-location: netmgmt\net_validate_authentication_input_arg.htm
tech.root: NetMgmt
ms.assetid: b7466e8a-81d8-4552-adff-47fc2f3ed3ad
ms.date: 12/05/2018
ms.keywords: '*PNET_VALIDATE_AUTHENTICATION_INPUT_ARG, NET_VALIDATE_AUTHENTICATION_INPUT_ARG, NET_VALIDATE_AUTHENTICATION_INPUT_ARG structure [Network Management], PNET_VALIDATE_AUTHENTICATION_INPUT_ARG, PNET_VALIDATE_AUTHENTICATION_INPUT_ARG structure pointer [Network Management], lmaccess/NET_VALIDATE_AUTHENTICATION_INPUT_ARG, lmaccess/PNET_VALIDATE_AUTHENTICATION_INPUT_ARG, netmgmt.net_validate_authentication_input_arg'
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
req.typenames: NET_VALIDATE_AUTHENTICATION_INPUT_ARG, *PNET_VALIDATE_AUTHENTICATION_INPUT_ARG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NET_VALIDATE_AUTHENTICATION_INPUT_ARG
 - lmaccess/_NET_VALIDATE_AUTHENTICATION_INPUT_ARG
 - PNET_VALIDATE_AUTHENTICATION_INPUT_ARG
 - lmaccess/PNET_VALIDATE_AUTHENTICATION_INPUT_ARG
 - NET_VALIDATE_AUTHENTICATION_INPUT_ARG
 - lmaccess/NET_VALIDATE_AUTHENTICATION_INPUT_ARG
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
 - NET_VALIDATE_AUTHENTICATION_INPUT_ARG
---

# NET_VALIDATE_AUTHENTICATION_INPUT_ARG structure


## -description

A client application passes the <b>NET_VALIDATE_AUTHENTICATION_INPUT_ARG</b> structure to the <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a> function when the application requests an authentication validation.

## -struct-fields

### -field InputPersistedFields

Specifies a <a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_persisted_fields">NET_VALIDATE_PERSISTED_FIELDS</a> structure that contains persistent password-related information about the account being logged on.

### -field PasswordMatched

BOOLEAN value that indicates the result of the client application's authentication of the password supplied by the user. If this parameter is <b>FALSE</b>, the password has not been authenticated.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>