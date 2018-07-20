---
UID: NS:wincrypt._PROV_ENUMALGS
title: "_PROV_ENUMALGS"
author: windows-sdk-content
description: Used with the CryptGetProvParam function when the PP_ENUMALGS parameter is retrieved to contain information about an algorithm supported by a cryptographic service provider (CSP).
old-location: security\prov_enumalgs.htm
old-project: seccrypto
ms.assetid: 8301d07f-88aa-49b4-9091-8f515b585c57
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PROV_ENUMALGS, PROV_ENUMALGS structure [Security], _PROV_ENUMALGS, _crypto2_prov_enumalgs, security.prov_enumalgs, wincrypt/PROV_ENUMALGS
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
req.typenames: PROV_ENUMALGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - PROV_ENUMALGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _PROV_ENUMALGS structure


## -description


The <b>PROV_ENUMALGS</b> structure is used with the <a href="https://msdn.microsoft.com/c0b7c1c8-aa42-4d40-a7f7-99c0821c8977">CryptGetProvParam</a> function when the <b>PP_ENUMALGS</b> parameter is retrieved to contain information about an algorithm supported by a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP).


## -struct-fields




### -field aiAlgid


						One of the <a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a> values that identifies the algorithm.


### -field dwBitLen

The default <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key length</a>, in bits, of the algorithm.


### -field dwNameLen

The length, in <b>CHAR</b>s, of the <b>szName</b> string. This length includes the terminating null character.


### -field szName

A null-terminated ANSI string that contains the name of the algorithm.

