---
UID: NF:tapi3if.ITAddressTranslation.TranslateDialog
title: ITAddressTranslation::TranslateDialog
author: windows-sdk-content
description: The TranslateDialog method displays an application-modal dialog box that allows the user to change the current location of a phone number about to be dialed, adjust location and calling card parameters, and see the effect.
old-location: tapi3\itaddresstranslation_translatedialog.htm
old-project: tapi
ms.assetid: fe744658-b5a7-4d22-bf8b-9c669be3da1e
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITAddressTranslation interface [TAPI 2.2],TranslateDialog method, ITAddressTranslation.TranslateDialog, ITAddressTranslation::TranslateDialog, TranslateDialog, TranslateDialog method [TAPI 2.2], TranslateDialog method [TAPI 2.2],ITAddressTranslation interface, _tapi3_itaddresstranslation_translatedialog, tapi3.itaddresstranslation_translatedialog, tapi3if/ITAddressTranslation::TranslateDialog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddressTranslation.TranslateDialog
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for <i>pAddressIn</i> and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.

The 
<b>TranslateDialog</b> method is a COM wrapper for the TAPI 2.1 
<a href="https://msdn.microsoft.com/c9fd7abb-3b4b-442b-badc-371a12724f67">LineTranslateDialog</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/e1cd88f1-1ed7-4e7f-a745-9a9c4af69317">ITAddressTranslation</a>



<a href="https://msdn.microsoft.com/c9fd7abb-3b4b-442b-badc-371a12724f67">LineTranslateDialog</a>
 

 

