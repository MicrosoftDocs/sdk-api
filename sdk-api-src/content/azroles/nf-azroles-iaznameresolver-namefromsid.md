---
UID: NF:azroles.IAzNameResolver.NameFromSid
title: IAzNameResolver::NameFromSid (azroles.h)
description: Gets the display name that corresponds to the specified security identifier (SID).
helpviewer_keywords: ["IAzNameResolver interface [Security]","NameFromSid method","IAzNameResolver.NameFromSid","IAzNameResolver::NameFromSid","NameFromSid","NameFromSid method [Security]","NameFromSid method [Security]","IAzNameResolver interface","azroles/IAzNameResolver::NameFromSid","security.iaznameresolver_namefromsid_method"]
old-location: security\iaznameresolver_namefromsid_method.htm
tech.root: security
ms.assetid: 3518e620-85cf-4bae-8366-d43564535774
ms.date: 12/05/2018
ms.keywords: IAzNameResolver interface [Security],NameFromSid method, IAzNameResolver.NameFromSid, IAzNameResolver::NameFromSid, NameFromSid, NameFromSid method [Security], NameFromSid method [Security],IAzNameResolver interface, azroles/IAzNameResolver::NameFromSid, security.iaznameresolver_namefromsid_method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzNameResolver::NameFromSid
 - azroles/IAzNameResolver::NameFromSid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzNameResolver.NameFromSid
---

# IAzNameResolver::NameFromSid


## -description

The <b>NameFromSid</b> method gets the display name that corresponds to the specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

## -parameters

### -param bstrSid [in]

The string representation of the SID to translate.

### -param pSidType [out]

An element of the <a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SID_NAME_USE</a> enumeration that specifies the type of SID being translated.

### -param pbstrName [out]

A pointer to the display name of the principal that corresponds to the SID specified by the <i>bstrSid</i> parameter.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. In particular, if the method cannot find the display name of the principal, it returns <b>CO_E_NOMATCHINGNAMEFOUND</b>. For a list of other common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.