---
UID: NS:wincrypt._CMC_ADD_EXTENSIONS_INFO
title: "_CMC_ADD_EXTENSIONS_INFO"
author: windows-sdk-content
description: Contains certificate extension control attributes to be added to a certificate.
old-location: security\cmc_add_extensions_info.htm
old-project: seccrypto
ms.assetid: 46fbea57-8a9d-48f3-8b65-8f28a843d6d9
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: "*PCMC_ADD_EXTENSIONS_INFO, CMC_ADD_EXTENSIONS_INFO, CMC_ADD_EXTENSIONS_INFO structure [Security], PCMC_ADD_EXTENSIONS_INFO, PCMC_ADD_EXTENSIONS_INFO structure pointer [Security], _CMC_ADD_EXTENSIONS_INFO, _crypto2_cmc_add_extensions_info, security.cmc_add_extensions_info, wincrypt/CMC_ADD_EXTENSIONS_INFO, wincrypt/PCMC_ADD_EXTENSIONS_INFO"
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
req.typenames: CMC_ADD_EXTENSIONS_INFO, *PCMC_ADD_EXTENSIONS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CMC_ADD_EXTENSIONS_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CMC_ADD_EXTENSIONS_INFO structure


## -description


The <b>CMC_ADD_EXTENSIONS_INFO</b> structure contains certificate extension control attributes to be added to a certificate.


## -struct-fields




### -field dwCmcDataReference

<b>DWORD</b> data reference number.


### -field cCertReference

<b>DWORD</b> count of elements in the <b>rgdwCertReference</b> array.


### -field rgdwCertReference

Array of certificate reference numbers.


### -field cExtension

<b>DWORD</b> count of the elements in the <b>rgExtension</b> array.


### -field rgExtension

Array of pointers to the 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> certificate extensions to be added.

