---
UID: NF:iwscapi.IWscProduct.get_RemediationPath
title: IWscProduct::get_RemediationPath (iwscapi.h)
description: Returns the current remediation path for the security product.
helpviewer_keywords: ["IWscProduct interface [Windows API]","get_RemediationPath method","IWscProduct.get_RemediationPath","IWscProduct::get_RemediationPath","get_RemediationPath","get_RemediationPath method [Windows API]","get_RemediationPath method [Windows API]","IWscProduct interface","iwscapi/IWscProduct::get_RemediationPath","winprog.iwscproduct_remediationpath"]
old-location: winprog\iwscproduct_remediationpath.htm
tech.root: winprog
ms.assetid: 6922B572-4E00-4B0B-BE1F-64343DD776A0
ms.date: 12/05/2018
ms.keywords: IWscProduct interface [Windows API],get_RemediationPath method, IWscProduct.get_RemediationPath, IWscProduct::get_RemediationPath, get_RemediationPath, get_RemediationPath method [Windows API], get_RemediationPath method [Windows API],IWscProduct interface, iwscapi/IWscProduct::get_RemediationPath, winprog.iwscproduct_remediationpath
req.header: iwscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wscapi.lib
req.dll: Wscapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWscProduct::get_RemediationPath
 - iwscapi/IWscProduct::get_RemediationPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wscapi.dll
api_name:
 - IWscProduct.get_RemediationPath
---

# IWscProduct::get_RemediationPath


## -description

Returns the current remediation path for the security product.

## -parameters

### -param pVal [out]

A pointer to the remediation path for the security product. This is displayed in the Windows Security Center user interface.

## -returns

If the method  succeeds, returns S_OK.

If the method  fails, returns a Win32 error code.

## -see-also

<a href="/windows/desktop/api/iwscapi/nn-iwscapi-iwscproduct">IWscProduct</a>