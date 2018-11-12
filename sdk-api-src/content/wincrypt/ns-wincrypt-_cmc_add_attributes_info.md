---
UID: NS:wincrypt._CMC_ADD_ATTRIBUTES_INFO
title: "_CMC_ADD_ATTRIBUTES_INFO"
author: windows-sdk-content
description: Contains certificate attributes to be added to a certificate.
old-location: security\cmc_add_attributes_info.htm
tech.root: seccrypto
ms.assetid: fd13cd2b-b818-41ca-85be-d51b864194df
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PCMC_ADD_ATTRIBUTES_INFO, CMC_ADD_ATTRIBUTES_INFO, CMC_ADD_ATTRIBUTES_INFO structure [Security], PCMC_ADD_ATTRIBUTES_INFO, PCMC_ADD_ATTRIBUTES_INFO structure pointer [Security], _CMC_ADD_ATTRIBUTES_INFO, _crypto2_cmc_add_attributes_info, security.cmc_add_attributes_info, wincrypt/CMC_ADD_ATTRIBUTES_INFO, wincrypt/PCMC_ADD_ATTRIBUTES_INFO"
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
 - CMC_ADD_ATTRIBUTES_INFO
product: Windows
targetos: Windows
req.typenames: CMC_ADD_ATTRIBUTES_INFO, *PCMC_ADD_ATTRIBUTES_INFO
req.redist: 
---

# _CMC_ADD_ATTRIBUTES_INFO structure


## -description


The <b>CMC_ADD_ATTRIBUTES_INFO</b> structure contains certificate attributes to be added to a certificate.


## -struct-fields




### -field dwCmcDataReference

<b>DWORD</b> data reference number.


### -field cCertReference

Count of elements in the <b>rgdwCertReference</b> array.


### -field rgdwCertReference

Array of certificate reference numbers.


### -field cAttribute

Count of the elements in the <b>rgAttribute</b> array.


### -field rgAttribute

Array of pointers to the 
<a href="https://msdn.microsoft.com/cdbaf38d-ddbe-4be0-afbc-f8bd76ef4847">CRYPT_ATTRIBUTE</a> certificate attributes to be added.

