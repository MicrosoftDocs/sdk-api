---
UID: NS:wintrust._CRYPT_TRUST_REG_ENTRY
title: CRYPT_TRUST_REG_ENTRY (wintrust.h)
description: Identifies a provider function by DLL name and function name.
helpviewer_keywords: ["*PCRYPT_TRUST_REG_ENTRY","CRYPT_TRUST_REG_ENTRY","CRYPT_TRUST_REG_ENTRY structure [Security]","PCRYPT_TRUST_REG_ENTRY","PCRYPT_TRUST_REG_ENTRY structure pointer [Security]","security.crypt_trust_reg_entry","wintrust/CRYPT_TRUST_REG_ENTRY","wintrust/PCRYPT_TRUST_REG_ENTRY"]
old-location: security\crypt_trust_reg_entry.htm
tech.root: security
ms.assetid: 1a531219-f254-4057-934b-af95bfe0bb83
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_TRUST_REG_ENTRY, CRYPT_TRUST_REG_ENTRY, CRYPT_TRUST_REG_ENTRY structure [Security], PCRYPT_TRUST_REG_ENTRY, PCRYPT_TRUST_REG_ENTRY structure pointer [Security], security.crypt_trust_reg_entry, wintrust/CRYPT_TRUST_REG_ENTRY, wintrust/PCRYPT_TRUST_REG_ENTRY'
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
req.typenames: CRYPT_TRUST_REG_ENTRY, *PCRYPT_TRUST_REG_ENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_TRUST_REG_ENTRY
 - wintrust/_CRYPT_TRUST_REG_ENTRY
 - PCRYPT_TRUST_REG_ENTRY
 - wintrust/PCRYPT_TRUST_REG_ENTRY
 - CRYPT_TRUST_REG_ENTRY
 - wintrust/CRYPT_TRUST_REG_ENTRY
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
 - CRYPT_TRUST_REG_ENTRY
---

# CRYPT_TRUST_REG_ENTRY structure


## -description

<p class="CCE_Message">[The <b>CRYPT_TRUST_REG_ENTRY</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_TRUST_REG_ENTRY</b> structure identifies a provider function by DLL name and function name. This structure is used by the <a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_register_actionid">CRYPT_REGISTER_ACTIONID</a> structure when the <a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustaddactionid">WintrustAddActionID</a> function is called.

## -struct-fields

### -field cbStruct

The size, in bytes, of this structure.

### -field pwszDLLName

A pointer to a null-terminated string for the DLL name.

### -field pwszFunctionName

A pointer to a null-terminated string for the function name.

## -see-also

<a href="/windows/desktop/api/wintrust/ns-wintrust-crypt_register_actionid">CRYPT_REGISTER_ACTIONID</a>



<a href="/windows/desktop/api/wintrust/nf-wintrust-wintrustaddactionid">WintrustAddActionID</a>