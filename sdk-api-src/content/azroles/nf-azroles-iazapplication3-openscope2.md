---
UID: NF:azroles.IAzApplication3.OpenScope2
title: IAzApplication3::OpenScope2 (azroles.h)
description: Opens an IAzScope2 object with the specified name.
helpviewer_keywords: ["IAzApplication3 interface [Security]","OpenScope2 method","IAzApplication3.OpenScope2","IAzApplication3::OpenScope2","OpenScope2","OpenScope2 method [Security]","OpenScope2 method [Security]","IAzApplication3 interface","azroles/IAzApplication3::OpenScope2","security.iazapplication3_openscope2"]
old-location: security\iazapplication3_openscope2.htm
tech.root: security
ms.assetid: 1ea9f12e-d00d-4ccd-bfd4-21027610e681
ms.date: 12/05/2018
ms.keywords: IAzApplication3 interface [Security],OpenScope2 method, IAzApplication3.OpenScope2, IAzApplication3::OpenScope2, OpenScope2, OpenScope2 method [Security], OpenScope2 method [Security],IAzApplication3 interface, azroles/IAzApplication3::OpenScope2, security.iazapplication3_openscope2
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
 - IAzApplication3::OpenScope2
 - azroles/IAzApplication3::OpenScope2
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
 - IAzApplication3.OpenScope2
---

# IAzApplication3::OpenScope2


## -description

The <b>OpenScope2</b> method opens an <a href="/windows/desktop/api/azroles/nn-azroles-iazscope2">IAzScope2</a> object with the specified name.

## -parameters

### -param bstrScopeName [in]

A string that contains the name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope2">IAzScope2</a> object to open.

### -param ppScope2 [out]

The address of a pointer to the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope2">IAzScope2</a> object that this method opens.

When you have finished using the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope2">IAzScope2</a> object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.