---
UID: NS:mssip.SIP_ADD_NEWPROVIDER_
title: SIP_ADD_NEWPROVIDER (mssip.h)
description: Defines a subject interface package (SIP). This structure is used by the CryptSIPAddProvider function.
helpviewer_keywords: ["*PSIP_ADD_NEWPROVIDER","PSIP_ADD_NEWPROVIDER","PSIP_ADD_NEWPROVIDER structure pointer [Security]","SIP_ADD_NEWPROVIDER","SIP_ADD_NEWPROVIDER structure [Security]","mssip/PSIP_ADD_NEWPROVIDER","mssip/SIP_ADD_NEWPROVIDER","security.sip_add_newprovider"]
old-location: security\sip_add_newprovider.htm
tech.root: security
ms.assetid: 5ca88c0c-a7c9-4517-a874-49d38c1bc7c3
ms.date: 12/05/2018
ms.keywords: '*PSIP_ADD_NEWPROVIDER, PSIP_ADD_NEWPROVIDER, PSIP_ADD_NEWPROVIDER structure pointer [Security], SIP_ADD_NEWPROVIDER, SIP_ADD_NEWPROVIDER structure [Security], mssip/PSIP_ADD_NEWPROVIDER, mssip/SIP_ADD_NEWPROVIDER, security.sip_add_newprovider'
req.header: mssip.h
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
req.typenames: SIP_ADD_NEWPROVIDER, *PSIP_ADD_NEWPROVIDER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SIP_ADD_NEWPROVIDER_
 - mssip/SIP_ADD_NEWPROVIDER_
 - PSIP_ADD_NEWPROVIDER
 - mssip/PSIP_ADD_NEWPROVIDER
 - SIP_ADD_NEWPROVIDER
 - mssip/SIP_ADD_NEWPROVIDER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mssip.h
api_name:
 - SIP_ADD_NEWPROVIDER
---

# SIP_ADD_NEWPROVIDER structure


## -description

The <b>SIP_ADD_NEWPROVIDER</b> structure defines a <a href="/windows/desktop/SecGloss/s-gly">subject interface package</a> (SIP). This structure is used by the <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipaddprovider">CryptSIPAddProvider</a> function.

## -struct-fields

### -field cbStruct

The size, in bytes, of this structure. Set this value to <code>sizeof(SIP_ADD_NEWPROVIDER)</code>.

### -field pgSubject

Pointer to the GUID that identifies the SIP.

### -field pwszDLLFileName

Pointer to a null-terminated string that contains the name of the DLL file.

### -field pwszMagicNumber

This member is not used.

### -field pwszIsFunctionName

Pointer to a null-terminated string that contains the name of the function that determines whether the file contents are supported by this SIP. This member can be <b>NULL</b>. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nc-mssip-pfnisfilesupported">pfnIsFileSupported</a>.

### -field pwszGetFuncName

Pointer to a null-terminated string that contains the name of the function that retrieves the signed data. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipgetsigneddatamsg">CryptSIPGetSignedDataMsg</a>.

### -field pwszPutFuncName

Pointer to a null-terminated string that contains the name of the function that stores the <a href="/windows/desktop/SecGloss/a-gly">Authenticode</a> signature in the target file. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipputsigneddatamsg">CryptSIPPutSignedDataMsg</a>.

### -field pwszCreateFuncName

Pointer to a null-terminated string that contains the name of the function that creates the hash. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipcreateindirectdata">CryptSIPCreateIndirectData</a>.

### -field pwszVerifyFuncName

Pointer to a null-terminated string that contains the name of the function that verifies the hash. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipverifyindirectdata">CryptSIPVerifyIndirectData</a>.

### -field pwszRemoveFuncName

Pointer to a null-terminated string that contains the name of the function that removes the signed data. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nf-mssip-cryptsipremovesigneddatamsg">CryptSIPRemoveSignedDataMsg</a>.

### -field pwszIsFunctionNameFmt2

Pointer to a null-terminated string that contains the name of the function that determines whether the file name extension is supported by this SIP. This member can be <b>NULL</b>. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nc-mssip-pfnisfilesupportedname">pfnIsFileSupportedName</a>.

### -field pwszGetCapFuncName

Pointer to a null-terminated string that contains the name  of the function that determines the capabilities of the SIP. If this parameter is set to <b>NULL</b>, multiple signatures are not available for this SIP. The signature for this function pointer is described in <a href="/windows/desktop/api/mssip/nc-mssip-pcryptsipgetcaps">pCryptSIPGetCaps</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available.

## -see-also

<a href="/windows/desktop/api/mssip/nf-mssip-cryptsipaddprovider">CryptSIPAddProvider</a>