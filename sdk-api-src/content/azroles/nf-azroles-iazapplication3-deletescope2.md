---
UID: NF:azroles.IAzApplication3.DeleteScope2
title: IAzApplication3::DeleteScope2 (azroles.h)
description: Removes the specified IAzScope2 object from the IAzApplication3 object.
helpviewer_keywords: ["DeleteScope2","DeleteScope2 method [Security]","DeleteScope2 method [Security]","IAzApplication3 interface","IAzApplication3 interface [Security]","DeleteScope2 method","IAzApplication3.DeleteScope2","IAzApplication3::DeleteScope2","azroles/IAzApplication3::DeleteScope2","security.iazapplication3_deletescope2"]
old-location: security\iazapplication3_deletescope2.htm
tech.root: security
ms.assetid: f42f9288-896b-4034-a16c-3d555acea453
ms.date: 12/05/2018
ms.keywords: DeleteScope2, DeleteScope2 method [Security], DeleteScope2 method [Security],IAzApplication3 interface, IAzApplication3 interface [Security],DeleteScope2 method, IAzApplication3.DeleteScope2, IAzApplication3::DeleteScope2, azroles/IAzApplication3::DeleteScope2, security.iazapplication3_deletescope2
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
 - IAzApplication3::DeleteScope2
 - azroles/IAzApplication3::DeleteScope2
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
 - IAzApplication3.DeleteScope2
---

# IAzApplication3::DeleteScope2


## -description

The <b>DeleteScope2</b> method removes the specified <a href="/windows/desktop/api/azroles/nn-azroles-iazscope2">IAzScope2</a> object from the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication3">IAzApplication3</a> object.

## -parameters

### -param bstrScopeName [in]

A string that contains the name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope2">IAzScope2</a> object to remove.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If any references to an <a href="/windows/desktop/api/azroles/nn-azroles-iazscope2">IAzScope2</a> object have been deleted from the cache, you can no longer use that object. In C++, you must release references to deleted <b>IAzScope2</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.