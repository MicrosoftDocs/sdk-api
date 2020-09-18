---
UID: NF:azroles.IAzClientContext2.AddStringSids
title: IAzClientContext2::AddStringSids (azroles.h)
description: Adds an array of string representations of security identifiers (SIDs) to the client context.
helpviewer_keywords: ["AddStringSids","AddStringSids method [Security]","AddStringSids method [Security]","IAzClientContext2 interface","IAzClientContext2 interface [Security]","AddStringSids method","IAzClientContext2.AddStringSids","IAzClientContext2::AddStringSids","azroles/IAzClientContext2::AddStringSids","security.iazclientcontext2_addstringsids"]
old-location: security\iazclientcontext2_addstringsids.htm
tech.root: security
ms.assetid: ac437686-fefb-413e-9f53-eed6c1df5798
ms.date: 12/05/2018
ms.keywords: AddStringSids, AddStringSids method [Security], AddStringSids method [Security],IAzClientContext2 interface, IAzClientContext2 interface [Security],AddStringSids method, IAzClientContext2.AddStringSids, IAzClientContext2::AddStringSids, azroles/IAzClientContext2::AddStringSids, security.iazclientcontext2_addstringsids
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzClientContext2::AddStringSids
 - azroles/IAzClientContext2::AddStringSids
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzClientContext2.AddStringSids
---

# IAzClientContext2::AddStringSids


## -description

The <b>AddStringSids</b> method adds an array of string representations of <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs) to the client context.

## -parameters

### -param varStringSids [in]

The array of string representations of SIDs to add to the client context.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.