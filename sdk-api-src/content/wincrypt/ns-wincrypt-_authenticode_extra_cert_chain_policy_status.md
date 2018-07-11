---
UID: NS:wincrypt._AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS
title: "_AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS"
author: windows-sdk-content
description: The AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS structure holds additional Authenticode policy information for chain verification of files.
old-location: security\authenticode_extra_cert_chain_policy_status.htm
old-project: seccrypto
ms.assetid: bc123d07-0d59-49e0-b0e3-23dadb270347
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: "*PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS, AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS, AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS structure [Security], PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS, PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS structure pointer [Security], _AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS, _crypto2_authenticode_extra_cert_chain_policy_status, security.authenticode_extra_cert_chain_policy_status, wincrypt/AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS, wincrypt/PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS, *PAUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS structure


## -description


The <b>AUTHENTICODE_EXTRA_CERT_CHAIN_POLICY_STATUS</b> structure holds additional Authenticode policy information for chain verification of files.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field fCommercial

BOOL flag. If <b>TRUE</b>, a signer has been verified by a CA as meeting certain minimum financial standards.

