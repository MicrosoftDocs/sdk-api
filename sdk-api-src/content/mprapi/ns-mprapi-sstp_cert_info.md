---
UID: NS:mprapi._SSTP_CERT_INFO
title: SSTP_CERT_INFO (mprapi.h)
description: Contains information about a Secure Socket Tunneling Protocol (SSTP) based certificate.
helpviewer_keywords: ["*PSSTP_CERT_INFO","SSTP_CERT_INFO","SSTP_CERT_INFO structure [RAS]","mprapi/SSTP_CERT_INFO","rras.sstp_cert_info"]
old-location: rras\sstp_cert_info.htm
tech.root: RRAS
ms.assetid: 004fce6d-c617-4356-9a8f-f7b4fbb3d4c2
ms.date: 12/05/2018
ms.keywords: '*PSSTP_CERT_INFO, SSTP_CERT_INFO, SSTP_CERT_INFO structure [RAS], mprapi/SSTP_CERT_INFO, rras.sstp_cert_info'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: SSTP_CERT_INFO, *PSSTP_CERT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SSTP_CERT_INFO
 - mprapi/_SSTP_CERT_INFO
 - PSSTP_CERT_INFO
 - mprapi/PSSTP_CERT_INFO
 - SSTP_CERT_INFO
 - mprapi/SSTP_CERT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - SSTP_CERT_INFO
---

# SSTP_CERT_INFO structure


## -description

The <b>SSTP_CERT_INFO</b> structure  contains information about a Secure Socket Tunneling Protocol (SSTP) based certificate.

## -struct-fields

### -field isDefault

A value that is <b>TRUE</b> if this is the default mode, and <b>FALSE</b> otherwise.

<div class="alert"><b>Note</b>  Default mode is when the administrator has not explicitly configured the device and the SSTP service automatically chooses a valid certificate.</div>
<div> </div>

### -field certBlob

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure that contains the SSTP based certificate hash. 

The <b>cbData</b> member contains the length, in bytes, of the certificate hash in the <b>pbData</b> member. If <b>cbData</b> is zero, the SSTP certificate configuration is cleaned and the SSTP service automatically chooses a valid certificate. The hashing algorithm used to calculate <b>pbData</b> is defined by the <b>certAlgorithm</b> member of the <a href="/windows/desktop/api/mprapi/ns-mprapi-sstp_config_params">SSTP_CONFIG_PARAMS</a> structure.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_tunnel_config_params0">MPRAPI_TUNNEL_CONFIG_PARAMS</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-sstp_config_params">SSTP_CONFIG_PARAMS</a>