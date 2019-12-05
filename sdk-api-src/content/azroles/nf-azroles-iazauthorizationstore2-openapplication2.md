---
UID: NF:azroles.IAzAuthorizationStore2.OpenApplication2
title: IAzAuthorizationStore2::OpenApplication2 (azroles.h)
description: Opens the IAzApplication2 object with the specified name.
old-location: security\iazauthorizationstore2_openapplication2.htm
tech.root: SecAuthZ
ms.assetid: 8705ea59-2419-4af5-9cc2-591221e09073
ms.date: 12/05/2018
ms.keywords: IAzAuthorizationStore2 interface [Security],OpenApplication2 method, IAzAuthorizationStore2.OpenApplication2, IAzAuthorizationStore2::OpenApplication2, OpenApplication2, OpenApplication2 method [Security], OpenApplication2 method [Security],IAzAuthorizationStore2 interface, azroles/IAzAuthorizationStore2::OpenApplication2, security.iazauthorizationstore2_openapplication2
ms.topic: method
f1_keywords:
- azroles/IAzAuthorizationStore2.OpenApplication2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Azroles.dll
api_name:
- IAzAuthorizationStore2.OpenApplication2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzAuthorizationStore2::OpenApplication2


## -description


The <b>OpenApplication2</b> method opens the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication2">IAzApplication2</a> object with the specified name.


## -parameters




### -param bstrApplicationName [in]

The name of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication2">IAzApplication2</a> object to open.


### -param varReserved [in, optional]

Reserved for future use.


### -param ppApplication [out]

A pointer to a pointer to the opened <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplication2">IAzApplication2</a> object.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.



