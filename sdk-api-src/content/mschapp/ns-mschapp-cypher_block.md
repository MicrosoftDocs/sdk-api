---
UID: NS:mschapp._CYPHER_BLOCK
title: CYPHER_BLOCK (mschapp.h)
description: The CYPHER_BLOCK is the basic unit of storage for the one-way function (OWF) password hashes.
helpviewer_keywords: ["CYPHER_BLOCK","CYPHER_BLOCK structure [MS-CHAP]","_CYPHER_BLOCK","mschap.cypher_block","mschapp/CYPHER_BLOCK"]
old-location: mschap\cypher_block.htm
tech.root: MsChap
ms.assetid: eb0e38ed-8d12-4df2-be58-7ac18447121f
ms.date: 12/05/2018
ms.keywords: CYPHER_BLOCK, CYPHER_BLOCK structure [MS-CHAP], _CYPHER_BLOCK, mschap.cypher_block, mschapp/CYPHER_BLOCK
req.header: mschapp.h
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
req.typenames: CYPHER_BLOCK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CYPHER_BLOCK
 - mschapp/_CYPHER_BLOCK
 - CYPHER_BLOCK
 - mschapp/CYPHER_BLOCK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MsChapp.h
api_name:
 - CYPHER_BLOCK
---

# CYPHER_BLOCK structure


## -description

The <b>CYPHER_BLOCK</b> is the basic unit of storage for the one-way function (OWF) password hashes.

## -struct-fields

### -field data

An array of CHAR used to store the password hashes and cipher text passed by the MS-CHAP password management API.

## -see-also

<a href="/previous-versions/windows/desktop/mschap/ms-chap-password-management-structures">MS-CHAP Password Management Structures</a>