---
UID: NF:azroles.IAzApplication3.ScopeExists
title: IAzApplication3::ScopeExists (azroles.h)
description: Indicates whether the specified scope exists in this IAzApplication3 object.
helpviewer_keywords: ["IAzApplication3 interface [Security]","ScopeExists method","IAzApplication3.ScopeExists","IAzApplication3::ScopeExists","ScopeExists","ScopeExists method [Security]","ScopeExists method [Security]","IAzApplication3 interface","azroles/IAzApplication3::ScopeExists","security.iazapplication3_scopeexists"]
old-location: security\iazapplication3_scopeexists.htm
tech.root: security
ms.assetid: 585f8b16-e634-4ac6-a20a-214eea344b0a
ms.date: 12/05/2018
ms.keywords: IAzApplication3 interface [Security],ScopeExists method, IAzApplication3.ScopeExists, IAzApplication3::ScopeExists, ScopeExists, ScopeExists method [Security], ScopeExists method [Security],IAzApplication3 interface, azroles/IAzApplication3::ScopeExists, security.iazapplication3_scopeexists
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzApplication3::ScopeExists
 - azroles/IAzApplication3::ScopeExists
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
 - IAzApplication3.ScopeExists
---

# IAzApplication3::ScopeExists


## -description

The <b>ScopeExists</b> method indicates whether the specified scope exists in this <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication3">IAzApplication3</a> object.

## -parameters

### -param bstrScopeName [in]

A string that contains the name of the scope to be checked.

### -param pbExist [out]

<b>VARIANT_TRUE</b> if the specified scope exists in this <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication3">IAzApplication3</a> object; otherwise, <b>VARIANT_FALSE</b>.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.