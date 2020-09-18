---
UID: NF:azroles.IAzNameResolver.NamesFromSids
title: IAzNameResolver::NamesFromSids (azroles.h)
description: Gets the display names that correspond to the specified security identifiers (SIDs).
helpviewer_keywords: ["IAzNameResolver interface [Security]","NamesFromSids method","IAzNameResolver.NamesFromSids","IAzNameResolver::NamesFromSids","NamesFromSids","NamesFromSids method [Security]","NamesFromSids method [Security]","IAzNameResolver interface","azroles/IAzNameResolver::NamesFromSids","security.iaznameresolver_namesfromsids_method"]
old-location: security\iaznameresolver_namesfromsids_method.htm
tech.root: security
ms.assetid: fedf0164-51ca-480c-8e45-443e74fc5b13
ms.date: 12/05/2018
ms.keywords: IAzNameResolver interface [Security],NamesFromSids method, IAzNameResolver.NamesFromSids, IAzNameResolver::NamesFromSids, NamesFromSids, NamesFromSids method [Security], NamesFromSids method [Security],IAzNameResolver interface, azroles/IAzNameResolver::NamesFromSids, security.iaznameresolver_namesfromsids_method
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
 - IAzNameResolver::NamesFromSids
 - azroles/IAzNameResolver::NamesFromSids
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
 - IAzNameResolver.NamesFromSids
---

# IAzNameResolver::NamesFromSids


## -description

The <b>NamesFromSids</b> method gets the display names that correspond to the specified <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs).

## -parameters

### -param vSids [in]

An array of string representations of the SIDs to translate.

This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a string representation of a SID.

### -param pvSidTypes [out]

A pointer to an array of elements of the <a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SID_NAME_USE</a> enumeration that specify the types of SIDs being translated.

This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a <b>VT_I4</b> value that specifies an element of the <a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SID_NAME_USE</a> enumeration.

### -param pvNames [out]

A pointer to an array of strings that contain the display names of the principals that correspond to the SIDs specified by the <i>vSids</i> parameter. 

This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a display name. If a name could not be found for one or more of the SIDs, the corresponding array element contains an empty string.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. If the method cannot find the display names of any of the principals, it returns <b>CO_E_NOMATCHINGNAMEFOUND</b>. For a list of other common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.