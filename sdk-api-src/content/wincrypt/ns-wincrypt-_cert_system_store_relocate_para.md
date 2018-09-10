---
UID: NS:wincrypt._CERT_SYSTEM_STORE_RELOCATE_PARA
title: "_CERT_SYSTEM_STORE_RELOCATE_PARA"
author: windows-sdk-content
description: The CERT_SYSTEM_STORE_RELOCATE_PARA structure contains data to be passed to CertOpenStore when that function's dwFlags parameter is set to CERT_SYSTEM_STORE_RELOCATE_FLAG.
old-location: security\cert_system_store_relocate_para.htm
tech.root: seccrypto
ms.assetid: 3bcb9b64-b9cf-48b2-bfd1-0836b3d221af
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PCERT_SYSTEM_STORE_RELOCATE_PARA, CERT_SYSTEM_STORE_RELOCATE_PARA, CERT_SYSTEM_STORE_RELOCATE_PARA structure [Security], PCERT_SYSTEM_STORE_RELOCATE_PARA, PCERT_SYSTEM_STORE_RELOCATE_PARA structure pointer [Security], _CERT_SYSTEM_STORE_RELOCATE_PARA, _crypto2_cert_system_store_relocate_para, security.cert_system_store_relocate_para, wincrypt/CERT_SYSTEM_STORE_RELOCATE_PARA, wincrypt/PCERT_SYSTEM_STORE_RELOCATE_PARA"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_SYSTEM_STORE_RELOCATE_PARA
product: Windows
targetos: Windows
req.typenames: CERT_SYSTEM_STORE_RELOCATE_PARA, *PCERT_SYSTEM_STORE_RELOCATE_PARA
req.redist: 
---

# _CERT_SYSTEM_STORE_RELOCATE_PARA structure


## -description


The <b>CERT_SYSTEM_STORE_RELOCATE_PARA</b> structure contains data to be passed to 
<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a> when that function's <i>dwFlags</i> parameter is set to CERT_SYSTEM_STORE_RELOCATE_FLAG. It allows the application to specify not only the name of the store to be opened, but also registry hKey information indicating a registry location other than the default location.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.hKeyBase

A handle to registry hKey.


### -field DUMMYUNIONNAME.pvBase

A pointer to a void to allow the system store location's base to be passed in a number of different forms.


### -field DUMMYUNIONNAME2

 


### -field DUMMYUNIONNAME2.pvSystemStore

A pointer to a void to allow the name of the system store to be passed in various forms.


### -field DUMMYUNIONNAME2.pszSystemStore

A null-terminated <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ASCII</a> string that names the system store.


### -field DUMMYUNIONNAME2.pwszSystemStore

A null-terminated Unicode string that names the system store.


## -remarks



The relocate capability is used to access system stores persisted in the Group Policy Template (GPT). For example, the Group Policy Editor's MMC snap-in extension for managing group policy trust lists and certificates uses the GPT's base HKEY to call 
<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>.




## -see-also




<a href="https://msdn.microsoft.com/4edccbfe-c0a8-442b-b6b7-51ef598e7c90">CertOpenStore</a>
 

 

