---
UID: NS:mssip.SIP_ADD_NEWPROVIDER_
title: SIP_ADD_NEWPROVIDER_
author: windows-sdk-content
description: Defines a subject interface package (SIP). This structure is used by the CryptSIPAddProvider function.
old-location: security\sip_add_newprovider.htm
tech.root: seccrypto
ms.assetid: 5ca88c0c-a7c9-4517-a874-49d38c1bc7c3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PSIP_ADD_NEWPROVIDER, PSIP_ADD_NEWPROVIDER, PSIP_ADD_NEWPROVIDER structure pointer [Security], SIP_ADD_NEWPROVIDER, SIP_ADD_NEWPROVIDER structure [Security], SIP_ADD_NEWPROVIDER_, mssip/PSIP_ADD_NEWPROVIDER, mssip/SIP_ADD_NEWPROVIDER, security.sip_add_newprovider"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mssip.h
api_name:
 - SIP_ADD_NEWPROVIDER
product: Windows
targetos: Windows
req.typenames: SIP_ADD_NEWPROVIDER, *PSIP_ADD_NEWPROVIDER
req.redist: 
---

# SIP_ADD_NEWPROVIDER_ structure


## -description


The <b>SIP_ADD_NEWPROVIDER</b> structure defines a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP). This structure is used by the <a href="https://msdn.microsoft.com/99633c2f-e5ed-49e4-9c98-7501f66e5571">CryptSIPAddProvider</a> function.


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

Pointer to a null-terminated string that contains the name of the function that determines whether the file contents are supported by this SIP. This member can be <b>NULL</b>. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/cf12d057-328a-4975-b7e5-842c4ea2e760">pfnIsFileSupported</a>.


### -field pwszGetFuncName

Pointer to a null-terminated string that contains the name of the function that retrieves the signed data. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/e3fabaa7-2dda-4c6c-8d1a-3ee5363e10b5">CryptSIPGetSignedDataMsg</a>.


### -field pwszPutFuncName

Pointer to a null-terminated string that contains the name of the function that stores the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">Authenticode</a> signature in the target file. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/731f64bf-49f0-4799-b84a-9ca04292aa91">CryptSIPPutSignedDataMsg</a>.


### -field pwszCreateFuncName

Pointer to a null-terminated string that contains the name of the function that creates the hash. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/bb4ecc95-972f-415c-9722-59b00a27cddc">CryptSIPCreateIndirectData</a>.


### -field pwszVerifyFuncName

Pointer to a null-terminated string that contains the name of the function that verifies the hash. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/137b8858-a31f-4ef6-96bd-c5e26ae7b3e8">CryptSIPVerifyIndirectData</a>.


### -field pwszRemoveFuncName

Pointer to a null-terminated string that contains the name of the function that removes the signed data. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/c3ea46bb-931a-4ca6-93f5-db7e07b4cb7a">CryptSIPRemoveSignedDataMsg</a>.


### -field pwszIsFunctionNameFmt2

Pointer to a null-terminated string that contains the name of the function that determines whether the file name extension is supported by this SIP. This member can be <b>NULL</b>. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/cc2304ef-c319-45eb-b2ec-7410510af213">pfnIsFileSupportedName</a>.


### -field pwszGetCapFuncName

Pointer to a null-terminated string that contains the name  of the function that determines the capabilities of the SIP. If this parameter is set to <b>NULL</b>, multiple signatures are not available for this SIP. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/8EA46B67-F542-4B15-81F4-3DD83DD45764">pCryptSIPGetCaps</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This member is not available.


## -see-also




<a href="https://msdn.microsoft.com/99633c2f-e5ed-49e4-9c98-7501f66e5571">CryptSIPAddProvider</a>
 

 

