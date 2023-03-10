---
UID: NF:azroles.IAzObjectPicker.GetPrincipals
title: IAzObjectPicker::GetPrincipals (azroles.h)
description: Displays a dialog box from which users can choose one or more principals, and then returns the chosen list of principals and their corresponding security identifiers (SIDs).
helpviewer_keywords: ["GetPrincipals","GetPrincipals method [Security]","GetPrincipals method [Security]","IAzObjectPicker interface","IAzObjectPicker interface [Security]","GetPrincipals method","IAzObjectPicker.GetPrincipals","IAzObjectPicker::GetPrincipals","azroles/IAzObjectPicker::GetPrincipals","security.iazobjectpicker_getprincipals_method"]
old-location: security\iazobjectpicker_getprincipals_method.htm
tech.root: security
ms.assetid: e03a2160-42bc-44a9-a893-36d2d1de18d4
ms.date: 12/05/2018
ms.keywords: GetPrincipals, GetPrincipals method [Security], GetPrincipals method [Security],IAzObjectPicker interface, IAzObjectPicker interface [Security],GetPrincipals method, IAzObjectPicker.GetPrincipals, IAzObjectPicker::GetPrincipals, azroles/IAzObjectPicker::GetPrincipals, security.iazobjectpicker_getprincipals_method
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
 - IAzObjectPicker::GetPrincipals
 - azroles/IAzObjectPicker::GetPrincipals
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
 - IAzObjectPicker.GetPrincipals
---

# IAzObjectPicker::GetPrincipals


## -description

The <b>GetPrincipals</b> method displays a dialog box from which users can choose one or more principals, and then returns the chosen list of principals and their corresponding <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs).

## -parameters

### -param hParentWnd [in]

A handle to the parent window of the dialog box.

### -param bstrTitle [in]

The display title of the dialog box.

### -param pvSidTypes [out]

A pointer to an array of elements of the <a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SID_NAME_USE</a> enumeration that specify the types of the SIDs that correspond to the principals chosen by the user.

This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a <b>VT_I4</b> value that specifies an element of the <a href="/windows/desktop/api/winnt/ne-winnt-sid_name_use">SID_NAME_USE</a> enumeration.

### -param pvNames [out]

A pointer to an array of display names of the principals chosen by the user. 

This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a display name.

### -param pvSids [out]

A pointer to an array of string representations of the SIDs that correspond to the principals chosen by the user.

This is a variant that contains either a <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> or the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object. Each element of the array holds a <b>VT_BSTR</b> that contains a string representation of a SID.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.