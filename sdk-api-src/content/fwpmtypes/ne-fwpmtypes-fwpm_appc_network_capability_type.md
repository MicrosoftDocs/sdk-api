---
UID: NE:fwpmtypes.FWPM_APPC_NETWORK_CAPABILITY_TYPE_
title: FWPM_APPC_NETWORK_CAPABILITY_TYPE (fwpmtypes.h)
description: Specifies the type of app container network capability that is associated with the object or traffic in question.
helpviewer_keywords: ["FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT","FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT_SERVER","FWPM_APPC_NETWORK_CAPABILITY_INTERNET_PRIVATE_NETWORK","FWPM_APPC_NETWORK_CAPABILITY_TYPE","FWPM_APPC_NETWORK_CAPABILITY_TYPE enumeration [Filtering]","fwp.fwpm_appc_network_capability_type","fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT","fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT_SERVER","fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_INTERNET_PRIVATE_NETWORK","fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_TYPE"]
old-location: fwp\fwpm_appc_network_capability_type.htm
tech.root: fwp
ms.assetid: e69ac412-0868-49da-9a87-58a03098839d
ms.date: 12/05/2018
ms.keywords: FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT, FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT_SERVER, FWPM_APPC_NETWORK_CAPABILITY_INTERNET_PRIVATE_NETWORK, FWPM_APPC_NETWORK_CAPABILITY_TYPE, FWPM_APPC_NETWORK_CAPABILITY_TYPE enumeration [Filtering], fwp.fwpm_appc_network_capability_type, fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT, fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT_SERVER, fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_INTERNET_PRIVATE_NETWORK, fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_TYPE
req.header: fwpmtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fwpmtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FWPM_APPC_NETWORK_CAPABILITY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FWPM_APPC_NETWORK_CAPABILITY_TYPE_
 - fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_TYPE_
 - FWPM_APPC_NETWORK_CAPABILITY_TYPE
 - fwpmtypes/FWPM_APPC_NETWORK_CAPABILITY_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fwpmtypes.h
api_name:
 - FWPM_APPC_NETWORK_CAPABILITY_TYPE
---

# FWPM_APPC_NETWORK_CAPABILITY_TYPE enumeration


## -description

The <b>FWPM_APPC_NETWORK_CAPABILITY_TYPE</b> enumeration specifies the type of app container network capability that is associated with the object or traffic in question.

## -enum-fields

### -field FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT:0

Allows the app container to make network requests to servers on the Internet. It acts as a client.

### -field FWPM_APPC_NETWORK_CAPABILITY_INTERNET_CLIENT_SERVER

Allows the app container to make requests and to receive requests to and from the Internet. It acts as a client and also as a server.

### -field FWPM_APPC_NETWORK_CAPABILITY_INTERNET_PRIVATE_NETWORK

Allows the app container to make requests and to receive requests to and from private networks (such as a home network, work network, or the corporate domain network of the computer). It acts as a client and also as a server.

## -see-also

<a href="/windows/desktop/FWP/fwp-enums">Windows Filtering Platform API Enumerated Types</a>
