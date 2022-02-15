---
UID: NE:netfw._NETISO_ERROR_TYPE
title: NETISO_ERROR_TYPE (netfw.h)
description: Specifies the type of error related to a network isolation operation.
helpviewer_keywords: ["NETISO_ERROR_TYPE","NETISO_ERROR_TYPE enumeration [ICS/ICF]","NETISO_ERROR_TYPE_INTERNET_CLIENT","NETISO_ERROR_TYPE_INTERNET_CLIENT_SERVER","NETISO_ERROR_TYPE_MAX","NETISO_ERROR_TYPE_NONE","NETISO_ERROR_TYPE_PRIVATE_NETWORK","ics.netiso_error_type","networkisolation/NETISO_ERROR_TYPE","networkisolation/NETISO_ERROR_TYPE_INTERNET_CLIENT","networkisolation/NETISO_ERROR_TYPE_INTERNET_CLIENT_SERVER","networkisolation/NETISO_ERROR_TYPE_MAX","networkisolation/NETISO_ERROR_TYPE_NONE","networkisolation/NETISO_ERROR_TYPE_PRIVATE_NETWORK"]
old-location: ics\netiso_error_type.htm
tech.root: ics
ms.assetid: 0daa9d07-8a65-4254-b197-a37e6e04ce32
ms.date: 12/05/2018
ms.keywords: NETISO_ERROR_TYPE, NETISO_ERROR_TYPE enumeration [ICS/ICF], NETISO_ERROR_TYPE_INTERNET_CLIENT, NETISO_ERROR_TYPE_INTERNET_CLIENT_SERVER, NETISO_ERROR_TYPE_MAX, NETISO_ERROR_TYPE_NONE, NETISO_ERROR_TYPE_PRIVATE_NETWORK, ics.netiso_error_type, networkisolation/NETISO_ERROR_TYPE, networkisolation/NETISO_ERROR_TYPE_INTERNET_CLIENT, networkisolation/NETISO_ERROR_TYPE_INTERNET_CLIENT_SERVER, networkisolation/NETISO_ERROR_TYPE_MAX, networkisolation/NETISO_ERROR_TYPE_NONE, networkisolation/NETISO_ERROR_TYPE_PRIVATE_NETWORK
req.header: netfw.h
req.include-header: Netfw.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: NETISO_ERROR_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NETISO_ERROR_TYPE
 - netfw/_NETISO_ERROR_TYPE
 - NETISO_ERROR_TYPE
 - netfw/NETISO_ERROR_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - networkisolation.h
api_name:
 - NETISO_ERROR_TYPE
---

# NETISO_ERROR_TYPE enumeration


## -description

The <b>NETISO_ERROR_TYPE</b> enumerated type specifies the type of error related to a network isolation operation.

## -enum-fields

### -field NETISO_ERROR_TYPE_NONE:0x00

No error.

### -field NETISO_ERROR_TYPE_PRIVATE_NETWORK:0x01

The failure was caused because the privateNetworkClientServer capability is missing.

### -field NETISO_ERROR_TYPE_INTERNET_CLIENT:0x02

The failure was caused because the internetClient capability is missing.

### -field NETISO_ERROR_TYPE_INTERNET_CLIENT_SERVER:0x03

The failure was caused because the internetClientServer capability is missing.

### -field NETISO_ERROR_TYPE_MAX:0x04

Maximum value for testing purposes.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo">NetworkIsolationDiagnoseConnectFailureAndGetInfo</a>
