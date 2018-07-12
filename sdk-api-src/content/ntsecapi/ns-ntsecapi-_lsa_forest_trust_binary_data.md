---
UID: NS:ntsecapi._LSA_FOREST_TRUST_BINARY_DATA
title: "_LSA_FOREST_TRUST_BINARY_DATA"
author: windows-sdk-content
description: Contains binary data used in Local Security Authority forest trust operations.
old-location: security\lsa_forest_trust_binary_data.htm
old-project: SecAuthN
ms.assetid: 2ddcf54e-c30f-4146-8cb6-71fcdd42ae68
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: "*PLSA_FOREST_TRUST_BINARY_DATA, LSA_FOREST_TRUST_BINARY_DATA, LSA_FOREST_TRUST_BINARY_DATA structure [Security], PLSA_FOREST_TRUST_BINARY_DATA, PLSA_FOREST_TRUST_BINARY_DATA structure pointer [Security], _LSA_FOREST_TRUST_BINARY_DATA, ntsecapi/LSA_FOREST_TRUST_BINARY_DATA, ntsecapi/PLSA_FOREST_TRUST_BINARY_DATA, security.lsa_forest_trust_binary_data"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: LSA_FOREST_TRUST_BINARY_DATA, *PLSA_FOREST_TRUST_BINARY_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - LSA_FOREST_TRUST_BINARY_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _LSA_FOREST_TRUST_BINARY_DATA structure


## -description


The <b>LSA_FOREST_TRUST_BINARY_DATA</b> structure contains binary data used in <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> forest trust operations.


## -struct-fields




### -field Length.range

 


### -field Length.range.0

 


### -field Length.range.MAX_FOREST_TRUST_BINARY_DATA_SIZE

 


### -field Buffer.size_is

 


### -field Buffer.size_is.Length

 


### -field Length

Size of the structure in bytes.


### -field Buffer

Pointer to an array of type <b>UCHAR</b> that contains the binary data. The buffer can contain at most 128 KB of data.

