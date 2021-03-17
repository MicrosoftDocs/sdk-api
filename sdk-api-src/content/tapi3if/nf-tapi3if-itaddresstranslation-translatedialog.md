---
UID: NF:tapi3if.ITAddressTranslation.TranslateDialog
title: ITAddressTranslation::TranslateDialog (tapi3if.h)
description: The TranslateDialog method displays an application-modal dialog box that allows the user to change the current location of a phone number about to be dialed, adjust location and calling card parameters, and see the effect.
helpviewer_keywords: ["ITAddressTranslation interface [TAPI 2.2]","TranslateDialog method","ITAddressTranslation.TranslateDialog","ITAddressTranslation::TranslateDialog","TranslateDialog","TranslateDialog method [TAPI 2.2]","TranslateDialog method [TAPI 2.2]","ITAddressTranslation interface","_tapi3_itaddresstranslation_translatedialog","tapi3.itaddresstranslation_translatedialog","tapi3if/ITAddressTranslation::TranslateDialog"]
old-location: tapi3\itaddresstranslation_translatedialog.htm
tech.root: tapi3
ms.assetid: fe744658-b5a7-4d22-bf8b-9c669be3da1e
ms.date: 12/05/2018
ms.keywords: ITAddressTranslation interface [TAPI 2.2],TranslateDialog method, ITAddressTranslation.TranslateDialog, ITAddressTranslation::TranslateDialog, TranslateDialog, TranslateDialog method [TAPI 2.2], TranslateDialog method [TAPI 2.2],ITAddressTranslation interface, _tapi3_itaddresstranslation_translatedialog, tapi3.itaddresstranslation_translatedialog, tapi3if/ITAddressTranslation::TranslateDialog
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAddressTranslation::TranslateDialog
 - tapi3if/ITAddressTranslation::TranslateDialog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddressTranslation.TranslateDialog
---

# ITAddressTranslation::TranslateDialog


## -description

The 
<b>TranslateDialog</b> method displays an application-modal dialog box that allows the user to change the current location of a phone number about to be dialed, adjust location and calling card parameters, and see the effect.

## -parameters

### -param hwndOwner [in]

A handle to a window to which the dialog box is to be attached. Can be a <b>NULL</b> value to indicate that any window created during the function should have no owner window.

### -param pAddressIn [in]

A pointer to <b>BSTR</b> containing a phone number that is used to show the effect of the user's changes on the location parameters. The number must be in canonical format. This pointer can be left <b>NULL</b>, in which case the phone number portion of the dialog box is not displayed. If the <i>pAddressIn</i> parameter contains a subaddress or name field or additional addresses separated from the first address by ASCII CR and LF characters, only the first address is used in the dialog box.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>hwndOwner</i> parameter is not a valid handle or the <i>pAddressIn</i> parameter is not a valid phone number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pAddressIn</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_REGISTRY_SETTING_CORRUPT</b></dt>
</dl>
</td>
<td width="60%">
The registry settings for address translation are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
No TSP exists that can do translation for this address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INUSE</b></dt>
</dl>
</td>
<td width="60%">
The dialog is already open and in use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALADDRESS</b></dt>
</dl>
</td>
<td width="60%">
The current address is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_OPERATIONFAILED</b></dt>
</dl>
</td>
<td width="60%">
TAPI was not able to complete the operation.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for <i>pAddressIn</i> and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

The 
<b>TranslateDialog</b> method is a COM wrapper for the TAPI 2.1 
<a href="/windows/desktop/api/tapi/nf-tapi-linetranslatedialog">LineTranslateDialog</a> function.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation">ITAddressTranslation</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linetranslatedialog">LineTranslateDialog</a>