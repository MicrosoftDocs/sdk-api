---
UID: NS:wincrypt._PROV_ENUMALGS_EX
title: "_PROV_ENUMALGS_EX"
author: windows-sdk-content
description: Used with the CryptGetProvParam function when the PP_ENUMALGS_EX parameter is retrieved to contain information about an algorithm supported by a cryptographic service provider (CSP).
old-location: security\prov_enumalgs_ex.htm
tech.root: seccrypto
ms.assetid: 239dbc6f-c3fa-4f97-aa9a-4993fe726a98
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: PROV_ENUMALGS_EX, PROV_ENUMALGS_EX structure [Security], _PROV_ENUMALGS_EX, _crypto2_prov_enumalgs_ex, security.prov_enumalgs_ex, wincrypt/PROV_ENUMALGS_EX
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
 - PROV_ENUMALGS_EX
product: Windows
targetos: Windows
req.typenames: PROV_ENUMALGS_EX
req.redist: 
---

# _PROV_ENUMALGS_EX structure


## -description


The <b>PROV_ENUMALGS_EX</b> structure is used with the <a href="https://msdn.microsoft.com/c0b7c1c8-aa42-4d40-a7f7-99c0821c8977">CryptGetProvParam</a> function when the <b>PP_ENUMALGS_EX</b> parameter is retrieved to contain information about an algorithm supported by a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP).


## -struct-fields




### -field aiAlgid

One of the <a href="https://msdn.microsoft.com/557436b4-f7f1-4708-acc7-c6b47e6322ad">ALG_ID</a> values that identifies the algorithm.


### -field dwDefaultLen

The default <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key length</a>, in bits, of the algorithm.


### -field dwMinLen

The minimum <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key length</a>, in bits, of the algorithm.


### -field dwMaxLen

The maximum <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key length</a>, in bits, of the algorithm.


### -field dwProtocols

Zero or a combination of one or more of the <a href="https://msdn.microsoft.com/61dc0eff-2033-464a-a558-1798a92d48a2">Protocol Flags</a> values that identifies the protocols supported by the algorithm.


### -field dwNameLen

The length, in <b>CHAR</b>s, of the <b>szName</b> string. This length includes the terminating null character.


### -field szName

A null-terminated ANSI string that contains the name of the algorithm.


### -field dwLongNameLen

The length, in <b>CHAR</b>s, of the <b>szLongName</b> string. This length includes the terminating null character.


### -field szLongName

A null-terminated ANSI string that contains the long name of the algorithm.

