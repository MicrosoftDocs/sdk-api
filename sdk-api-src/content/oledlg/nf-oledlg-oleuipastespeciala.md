---
UID: NF:oledlg.OleUIPasteSpecialA
title: OleUIPasteSpecialA function (oledlg.h)
description: Invokes the standard Paste Special dialog box, allowing the user to select the format of the clipboard object to be pasted or paste-linked. (ANSI)
helpviewer_keywords: ["OleUIPasteSpecialA", "oledlg/OleUIPasteSpecialA"]
old-location: com\oleuipastespecial.htm
tech.root: com
ms.assetid: fb1335da-a863-4d15-8a8d-289d8cccd13f
ms.date: 12/05/2018
ms.keywords: OleUIPasteSpecial, OleUIPasteSpecial function [COM], OleUIPasteSpecialA, OleUIPasteSpecialW, _ole_OleUIPasteSpecial, com.oleuipastespecial, oledlg/OleUIPasteSpecial, oledlg/OleUIPasteSpecialA, oledlg/OleUIPasteSpecialW
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OleUIPasteSpecialW (Unicode) and OleUIPasteSpecialA (ANSI)
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
 - OleUIPasteSpecialA
 - oledlg/OleUIPasteSpecialA
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
 - OleUIPasteSpecial
 - OleUIPasteSpecialA
 - OleUIPasteSpecialW
---

# OleUIPasteSpecialA function


## -description

Invokes the standard <b>Paste Special</b> dialog box, allowing the user to select the format of the clipboard object to be pasted or paste-linked.

## -parameters

### -param unnamedParam1 [in]

A pointer to an <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipastespeciala">OLEUIPASTESPECIAL</a> structure.

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
Unable to call <a href="/windows/desktop/api/winuser/nf-winuser-loadstringa">LoadString</a> to get localized resources from the library.

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
<dt><b>OLEUI_IOERR_SRCDATAOBJECTINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <b>lpSrcDataObject</b> member of <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipastespeciala">OLEUIPASTESPECIAL</a> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_IOERR_ARRPASTEENTRIESINVALID </b></dt>
</dl>
</td>
<td width="60%">
The <b>arrPasteEntries</b> member of <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipastespeciala">OLEUIPASTESPECIAL</a> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_IOERR_ARRLINKTYPESINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <b>arrLinkTypes</b> member of <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuipastespeciala">OLEUIPASTESPECIAL</a> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_PSERR_CLIPBOARDCHANGED</b></dt>
</dl>
</td>
<td width="60%">
The clipboard contents changed while the dialog box was displayed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_PSERR_GETCLIPBOAARDFAILED 

</b></dt>
</dl>
</td>
<td width="60%">
The <b>lpSrcDataObj</b> member is incorrect.


</td>
</tr>
</table>

## -remarks

The design of the <b>Paste Special</b> dialog box assumes that if you are willing to permit a user to link to an object, you are also willing to permit the user to embed that object. For this reason, if any of the OLEUIPASTE_LINKTYPE flags associated with the <a href="/windows/desktop/api/oledlg/ne-oledlg-oleuipasteflag">OLEUIPASTEFLAG</a> enumeration are set, then the OLEUIPASTE_PASTE flag must also be set in order for the data formats to appear in the <b>Paste Special</b> dialog box.



The text displayed in the <b>Source</b> field of the standard <b>Paste Special</b> dialog box, which is implemented in Oledlg32.dll, is the null-terminated string whose offset in bytes is specified in the <b>dwSrcofCopy</b> member of the <a href="/windows/desktop/api/oleidl/ns-oleidl-objectdescriptor">OBJECTDESCRIPTOR</a> structure for the object to be pasted. If an <b>OBJECTDESCRIPTOR</b> structure is not available for this object, the dialog box displays whatever text may be associated with CF_LINKSOURCEDESCRIPTOR. If neither structure is available, the dialog box looks for CF_FILENAME. If CF_FILENAME is not found, the dialog box displays the string "Unknown Source".

To free an <b>HMETAFILEPICT</b> returned from the <b>Insert Object</b> or <b>Paste Special</b> dialog box, delete the attached metafile on the handle, as follows.


``` syntax
void FreeHmetafilepict(HMETAFILEPICT hmfp)
{
    if (hmfp != NULL)
    {
        LPMETAFILEPICT pmfp = GlobalLock(hmfp);
 
        DeleteMetaFile(pmfp->hMF);
        GlobalUnlock(hmfp);
        GlobalFree(hmfp);
    }
    else
    {
        // Handle null pointers here.
        exit(0);
    }
}
```





> [!NOTE]
> The oledlg.h header defines OLEUIPASTESPECIAL as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/oledlg/ne-oledlg-oleuipasteflag">OLEUIPASTEFLAG</a>
