---
UID: NS:wintrust._CRYPT_TRUST_REG_ENTRY
title: CRYPT_TRUST_REG_ENTRY
author: windows-sdk-content
description: Identifies a provider function by DLL name and function name.
old-location: security\crypt_trust_reg_entry.htm
tech.root: seccrypto
ms.assetid: 1a531219-f254-4057-934b-af95bfe0bb83
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCRYPT_TRUST_REG_ENTRY, CRYPT_TRUST_REG_ENTRY, CRYPT_TRUST_REG_ENTRY structure [Security], PCRYPT_TRUST_REG_ENTRY, PCRYPT_TRUST_REG_ENTRY structure pointer [Security], security.crypt_trust_reg_entry, wintrust/CRYPT_TRUST_REG_ENTRY, wintrust/PCRYPT_TRUST_REG_ENTRY"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wintrust.h
api_name:
 - CRYPT_TRUST_REG_ENTRY
product: Windows
targetos: Windows
req.typenames: CRYPT_TRUST_REG_ENTRY, *PCRYPT_TRUST_REG_ENTRY
req.redist: 
---

# CRYPT_TRUST_REG_ENTRY structure


## -description


<p class="CCE_Message">[The <b>CRYPT_TRUST_REG_ENTRY</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPT_TRUST_REG_ENTRY</b> structure identifies a provider function by DLL name and function name. This structure is used by the <a href="https://msdn.microsoft.com/0b2b482f-f087-4be7-b17f-91c287c3460d">CRYPT_REGISTER_ACTIONID</a> structure when the <a href="https://msdn.microsoft.com/3b282342-9c86-42fa-b745-e5194d2885dc">WintrustAddActionID</a> function is called.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field pwszDLLName

A pointer to a null-terminated string for the DLL name.


### -field pwszFunctionName

A pointer to a null-terminated string for the function name.


## -see-also




<a href="https://msdn.microsoft.com/0b2b482f-f087-4be7-b17f-91c287c3460d">CRYPT_REGISTER_ACTIONID</a>



<a href="https://msdn.microsoft.com/3b282342-9c86-42fa-b745-e5194d2885dc">WintrustAddActionID</a>
 

 

