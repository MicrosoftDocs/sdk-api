---
UID: NF:azroles.IAzApplication2.InitializeClientContext2
title: IAzApplication2::InitializeClientContext2 (azroles.h)
description: Retrieves an IAzClientContext2 object pointer.
helpviewer_keywords: ["IAzApplication2 interface [Security]","InitializeClientContext2 method","IAzApplication2.InitializeClientContext2","IAzApplication2::InitializeClientContext2","InitializeClientContext2","InitializeClientContext2 method [Security]","InitializeClientContext2 method [Security]","IAzApplication2 interface","azroles/IAzApplication2::InitializeClientContext2","security.iazapplication2_initializeclientcontext2"]
old-location: security\iazapplication2_initializeclientcontext2.htm
tech.root: security
ms.assetid: 8790ebb0-97eb-47a0-b975-87e0524dcc1b
ms.date: 12/05/2018
ms.keywords: IAzApplication2 interface [Security],InitializeClientContext2 method, IAzApplication2.InitializeClientContext2, IAzApplication2::InitializeClientContext2, InitializeClientContext2, InitializeClientContext2 method [Security], InitializeClientContext2 method [Security],IAzApplication2 interface, azroles/IAzApplication2::InitializeClientContext2, security.iazapplication2_initializeclientcontext2
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzApplication2::InitializeClientContext2
 - azroles/IAzApplication2::InitializeClientContext2
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
 - IAzApplication2.InitializeClientContext2
---

# IAzApplication2::InitializeClientContext2


## -description

The <b>InitializeClientContext2</b> method retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext2">IAzClientContext2</a> object pointer.

## -parameters

### -param IdentifyingString [in]

A string that identifies the client context in the audit trail for client connection and object access audit entries.

### -param varReserved [in, optional]

Reserved for future use.

### -param ppClientContext [out]

A pointer to a pointer to the returned <a href="/windows/desktop/api/azroles/nn-azroles-iazclientcontext2">IAzClientContext2</a> object.

## -returns

 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.