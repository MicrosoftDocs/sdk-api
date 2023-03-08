---
UID: NF:keycredmgr.KeyCredentialManagerShowUIOperation
title: KeyCredentialManagerShowUIOperation function (keycredmgr.h)
description: API to perform the requested WHFB operation.
helpviewer_keywords: ["KeyCredentialManagerShowUIOperation","KeyCredentialManagerShowUIOperation function [Security]","keycredmgr/KeyCredentialManagerShowUIOperation","security.keycredentialmanagershowuioperation"]
old-location: security\keycredentialmanagershowuioperation.htm
tech.root: security
ms.assetid: 94AB2BA7-810C-4AC4-A719-FD9684C21BA0
ms.date: 12/05/2018
ms.keywords: KeyCredentialManagerShowUIOperation, KeyCredentialManagerShowUIOperation function [Security], keycredmgr/KeyCredentialManagerShowUIOperation, security.keycredentialmanagershowuioperation
req.header: keycredmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Keycredmgr.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - KeyCredentialManagerShowUIOperation
 - keycredmgr/KeyCredentialManagerShowUIOperation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - keycredmgr.lib
 - keycredmgr.dll
api_name:
 - KeyCredentialManagerShowUIOperation
---

# KeyCredentialManagerShowUIOperation function


## -description

API to perform the requested WHFB operation.

## -parameters

### -param hWndOwner [in]

Window handle of the calling app.

### -param keyCredentialManagerOperationType [in]

The intended operation from the <a href="/windows/win32/api/keycredmgr/ne-keycredmgr-keycredentialmanageroperationtype">KeyCredentialManagerOperationType</a>.

## -returns

Returns an HRESULT

