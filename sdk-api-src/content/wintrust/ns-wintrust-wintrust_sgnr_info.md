---
UID: NS:wintrust.WINTRUST_SGNR_INFO_
title: WINTRUST_SGNR_INFO (wintrust.h)
description: Used when calling WinVerifyTrust to verify a CMSG_SIGNER_INFO structure.
helpviewer_keywords: ["*PWINTRUST_SGNR_INFO","PWINTRUST_SGNR_INFO","PWINTRUST_SGNR_INFO structure pointer [Security]","WINTRUST_SGNR_INFO","WINTRUST_SGNR_INFO structure [Security]","_win32_wintrust_sgnr_info","security.wintrust_sgnr_info","wintrust/PWINTRUST_SGNR_INFO","wintrust/WINTRUST_SGNR_INFO"]
old-location: security\wintrust_sgnr_info.htm
tech.root: security
ms.assetid: 04e62bfa-efe4-428a-ae6b-58c2377fd5ba
ms.date: 12/05/2018
ms.keywords: '*PWINTRUST_SGNR_INFO, PWINTRUST_SGNR_INFO, PWINTRUST_SGNR_INFO structure pointer [Security], WINTRUST_SGNR_INFO, WINTRUST_SGNR_INFO structure [Security], _win32_wintrust_sgnr_info, security.wintrust_sgnr_info, wintrust/PWINTRUST_SGNR_INFO, wintrust/WINTRUST_SGNR_INFO'
req.header: wintrust.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WINTRUST_SGNR_INFO, *PWINTRUST_SGNR_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WINTRUST_SGNR_INFO_
 - wintrust/WINTRUST_SGNR_INFO_
 - PWINTRUST_SGNR_INFO
 - wintrust/PWINTRUST_SGNR_INFO
 - WINTRUST_SGNR_INFO
 - wintrust/WINTRUST_SGNR_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - WINTRUST_SGNR_INFO
---

# WINTRUST_SGNR_INFO structure


## -description

<p class="CCE_Message">[The  <b>WINTRUST_SGNR_INFO</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>WINTRUST_SGNR_INFO</b> structure is used when calling 
<a href="/windows/desktop/api/wintrust/nf-wintrust-winverifytrust">WinVerifyTrust</a> to verify a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_info">CMSG_SIGNER_INFO</a> structure.

## -struct-fields

### -field cbStruct

Count of bytes in this structure.

### -field pcwszDisplayName

String with the name representing the signer to be checked.

### -field psSignerInfo

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_info">CMSG_SIGNER_INFO</a> structure that includes the <a href="/windows/desktop/SecGloss/d-gly">signature</a> to be verified.

### -field chStores

Number of store handles in <b>pahStores</b>.

### -field pahStores

An array of open <a href="/windows/desktop/SecGloss/c-gly">certificate stores</a> to be added to the list of stores that the policy provider uses to find certificates while building a trust chain.