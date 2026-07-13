---
UID: NF:oledlg.OleUIConvertA
title: OleUIConvertA function (oledlg.h)
description: Invokes the standard Convert dialog box, allowing the user to change the type of a single specified object, or the type of all OLE objects of the specified object's class. (ANSI)
helpviewer_keywords: ["OleUIConvertA", "oledlg/OleUIConvertA"]
old-location: com\oleuiconvert.htm
tech.root: com
ms.assetid: 3af4b321-cea2-4f88-ae22-2dcefbb2c2ad
ms.date: 12/05/2018
ms.keywords: OleUIConvert, OleUIConvert function [COM], OleUIConvertA, OleUIConvertW, _ole_OleUIConvert, com.oleuiconvert, oledlg/OleUIConvert, oledlg/OleUIConvertA, oledlg/OleUIConvertW
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OleUIConvertW (Unicode) and OleUIConvertA (ANSI)
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
 - OleUIConvertA
 - oledlg/OleUIConvertA
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
 - OleUIConvert
 - OleUIConvertA
 - OleUIConvertW
---

# OleUIConvertA function


## -description

Invokes the standard <b>Convert</b> dialog box, allowing the user to change the type of a single specified object, or the type of all OLE objects of the specified object's class.

## -parameters

### -param unnamedParam1 [in]

Pointer to an <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiconverta">OLEUICONVERT</a> structure that contains information used to initialize the dialog box.

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
The user pressed the OK button.

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
The user pressed the Cancel button.

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
<dt><b>OLEUI_CTERR_CLASSIDINVALID</b></dt>
</dl>
</td>
<td width="60%">
A <b>clsid</b> value was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_CTERR_DVASPECTINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <b>dvAspect</b> value was invalid. This member specifies the aspect of the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_CTERR_CBFORMATINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <b>wFormat</b> value was invalid. This member specifies the data format of the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_CTERR_STRINGINVALID</b></dt>
</dl>
</td>
<td width="60%">
A string value (for example, <b>lpszUserType</b> or <b>lpszDefLabel</b>) was invalid.

</td>
</tr>
</table>

## -remarks

<b>OleUIConvert</b> populates the <b>Convert</b> dialog box's list box with object classes by traversing the registry and looking for entries in the Readable and ReadWritable keys. Every class that includes the original class' default file format in its Readable key is added to the Convert list, and every class that includes the original class' default file format in its ReadWritable key is added to the Activate As list. The Convert list is shown in the dialog box's list box when the <b>Convert</b> radio button is selected (the default selection), and the Activate As list is shown when <b>Activate As</b> is selected.



Note that you can change the type of all objects of a given class only when CF_CONVERTONLY is not specified.

The convert command, which invokes this function, should only be made available to the user if <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuicanconvertoractivateas">OleUICanConvertOrActivateAs</a> returns S_OK. 






> [!NOTE]
> The oledlg.h header defines OLEUICONVERT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiconverta">OLEUICONVERT</a>



<a href="/windows/desktop/api/oledlg/nf-oledlg-oleuicanconvertoractivateas">OleUICanConvertOrActivateAs</a>
