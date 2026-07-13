---
UID: NF:oledlg.OleUIObjectPropertiesW
title: OleUIObjectPropertiesW function (oledlg.h)
description: Invokes the Object Properties dialog box, which displays General, View, and Link information about an object. (Unicode)
helpviewer_keywords: ["OleUIObjectProperties", "OleUIObjectProperties function [COM]", "OleUIObjectPropertiesW", "_ole_OleUIObjectProperties", "com.oleuiobjectproperties", "oledlg/OleUIObjectProperties", "oledlg/OleUIObjectPropertiesW"]
old-location: com\oleuiobjectproperties.htm
tech.root: com
ms.assetid: 591f6056-2e5f-4e58-8806-9a0093de2463
ms.date: 12/05/2018
ms.keywords: OleUIObjectProperties, OleUIObjectProperties function [COM], OleUIObjectPropertiesA, OleUIObjectPropertiesW, _ole_OleUIObjectProperties, com.oleuiobjectproperties, oledlg/OleUIObjectProperties, oledlg/OleUIObjectPropertiesA, oledlg/OleUIObjectPropertiesW
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OleUIObjectPropertiesW (Unicode) and OleUIObjectPropertiesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleDlg.lib
req.dll: OleDlg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleUIObjectPropertiesW
 - oledlg/OleUIObjectPropertiesW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleDlg.dll
api_name:
 - OleUIObjectProperties
 - OleUIObjectPropertiesA
 - OleUIObjectPropertiesW
---

# OleUIObjectPropertiesW function


## -description

Invokes the <b>Object Properties</b> dialog box, which displays <b>General</b>, <b>View</b>, and <b>Link</b> information about an object.

## -parameters

### -param unnamedParam1 [in]

Pointer to the <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiobjectpropsa">OLEUIOBJECTPROPS</a> structure.

## -returns

Standard Success/Error Definitions



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Unknown failure (unused).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OK</b></dt>
</dl>
</td>
<td width="60%">
The user pressed the <b>OK</b> button.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
No error, same as OLEUI_OK.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
The user pressed the <b>Cancel</b> button.

</td>
</tr>
</table>
 


Standard Field Validation Errors



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_STANDARDMIN</b></dt>
</dl>
</td>
<td width="60%">
Errors common to all dialog boxes lie in the range OLEUI_ERR_STANDARDMIN to OLEUI_ERR_STANDARDMAX. This value allows the application to test for standard messages in order to display error messages to the user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_STRUCTURENULL</b></dt>
</dl>
</td>
<td width="60%">
The pointer to an OLEUIXXX structure passed into the function was <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_STRUCTUREINVALID</b></dt>
</dl>
</td>
<td width="60%">
Insufficient permissions for read or write access to an OLEUIXXX structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_CBSTRUCTINCORRECT</b></dt>
</dl>
</td>
<td width="60%">
The <i>cbstruct</i> value is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_HWNDOWNERINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hWndOwner</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_LPSZCAPTIONINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpszCaption</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_LPFNHOOKINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpfnHook</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_HINSTANCEINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hInstance</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_LPSZTEMPLATEINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpszTemplate</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_HRESOURCEINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hResource</i> value is invalid.

</td>
</tr>
</table>
 

Initialization Errors


Initialization Errors



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_FINDTEMPLATEFAILURE</b></dt>
</dl>
</td>
<td width="60%">
Unable to find the dialog box template.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_LOADTEMPLATEFAILURE</b></dt>
</dl>
</td>
<td width="60%">
Unable to load the dialog box template.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_DIALOGFAILURE</b></dt>
</dl>
</td>
<td width="60%">
Dialog box initialization failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_LOCALMEMALLOC</b></dt>
</dl>
</td>
<td width="60%">
A call to <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> or the standard <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> allocator failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_GLOBALMEMALLOC</b></dt>
</dl>
</td>
<td width="60%">
A call to <a href="/windows/desktop/api/winbase/nf-winbase-globalalloc">GlobalAlloc</a> or the standard <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> allocator failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_LOADSTRING</b></dt>
</dl>
</td>
<td width="60%">
Unable to call LoadString for localized resources from the library.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_OLEMEMALLOC</b></dt>
</dl>
</td>
<td width="60%">
A call to the standard <a href="/windows/desktop/api/objidl/nn-objidl-imalloc">IMalloc</a> allocator failed.

</td>
</tr>
</table>
 


Function Specific Errors



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_STANDARDMAX</b></dt>
</dl>
</td>
<td width="60%">
Errors common to all dialog boxes lie in the range OLEUI_ERR_STANDARDMIN to OLEUI_ERR_STANDARDMAX. This value allows the application to test for standard messages in order to display error messages to the user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_SUBPROPNULL</b></dt>
</dl>
</td>
<td width="60%">
<i>lpGP</i> or <i>lpVP</i> is <b>NULL</b>, or <i>dwFlags</i> and OPF_OBJECTISLINK and <i>lpLP</i> are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_SUBPROPINVALID</b></dt>
</dl>
</td>
<td width="60%">
Insufficient write-access permissions for the structures pointed to by <i>lpGP</i>, <i>lpVP</i>, or <i>lpLP</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_PROPSHEETNULL</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpLP</i> value is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_PROPSHEETINVALID</b></dt>
</dl>
</td>
<td width="60%">
Insufficient write-access permissions for the structures pointed to by <i>lpGP</i>, <i>lpVP</i>, or <i>lpLP</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_SUPPROP</b></dt>
</dl>
</td>
<td width="60%">
The sub-link property pointer, <i>lpLP</i>, is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_PROPSINVALID</b></dt>
</dl>
</td>
<td width="60%">
Insufficient write access for the sub-link property pointer, <i>lpLP</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_PAGESINCORRECT</b></dt>
</dl>
</td>
<td width="60%">
Some sub-link properties of the <i>lpPS</i> member are incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_INVALIDPAGES</b></dt>
</dl>
</td>
<td width="60%">
Some sub-link properties of the <i>lpPS</i> member are incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
A sub-link property of the <i>lpPS</i> member is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_DLGPROCNOTNULL</b></dt>
</dl>
</td>
<td width="60%">
A sub-link property of the <i>lpPS</i> member is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_LPARAMNOTZERO</b></dt>
</dl>
</td>
<td width="60%">
A sub-link property of the <i>lpPS</i> member is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_GPERR_STRINGINVALID</b></dt>
</dl>
</td>
<td width="60%">
A string value (for example, <i>lplpszLabel</i> or <i>lplpszType</i>) is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_GPERR_CLASSIDINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>clsid</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_GPERR_LPCLSIDEXCLUDEINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>ClsidExcluded</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_GPERR_CBFORMATINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>wFormat</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_VPERR_METAPICTINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>hMetaPict</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_VPERR_DVASPECTINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>dvAspect</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_PROPERTYSHEET</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpPS</i> value is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_OBJINFOINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpObjInfo</i> value is <b>NULL</b> or the calling process doesn't have read access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_OPERR_LINKINFOINVALID 

</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpLinkInfo</i> value is <b>NULL</b> or the calling process doesn't have read access.


</td>
</tr>
</table>

## -remarks

<b>OleUIObjectProperties</b> is passed an <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiobjectpropsa">OLEUIOBJECTPROPS</a> structure, which supplies the information needed to fill in the <b>General</b>, <b>View</b>, and <b>Link</b> tabs of the <b>Object Properties</b> dialog box.





> [!NOTE]
> The oledlg.h header defines OleUIObjectProperties as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuilinkinfoa">IOleUILinkInfo</a>



<a href="/windows/desktop/api/oledlg/nn-oledlg-ioleuiobjinfoa">IOleUIObjInfo</a>



<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuignrlpropsa">OLEUIGNRLPROPS</a>



<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuilinkpropsa">OLEUILINKPROPS</a>



<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiobjectpropsa">OLEUIOBJECTPROPS</a>



<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiviewpropsa">OLEUIVIEWPROPS</a>
