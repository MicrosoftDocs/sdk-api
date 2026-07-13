---
UID: NF:oledlg.OleUIInsertObjectW
title: OleUIInsertObjectW function (oledlg.h)
description: Invokes the standard Insert Object dialog box, which allows the user to select an object source and class name, as well as the option of displaying the object as itself or as an icon. (Unicode)
helpviewer_keywords: ["OleUIInsertObject", "OleUIInsertObject function [COM]", "OleUIInsertObjectW", "_ole_OleUIInsertObject", "com.oleuiinsertobject", "oledlg/OleUIInsertObject", "oledlg/OleUIInsertObjectW"]
old-location: com\oleuiinsertobject.htm
tech.root: com
ms.assetid: f0ca8c0d-2538-4197-a830-d5ffb9f8b635
ms.date: 12/05/2018
ms.keywords: OleUIInsertObject, OleUIInsertObject function [COM], OleUIInsertObjectA, OleUIInsertObjectW, _ole_OleUIInsertObject, com.oleuiinsertobject, oledlg/OleUIInsertObject, oledlg/OleUIInsertObjectA, oledlg/OleUIInsertObjectW
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OleUIInsertObjectW (Unicode) and OleUIInsertObjectA (ANSI)
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
 - OleUIInsertObjectW
 - oledlg/OleUIInsertObjectW
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
 - OleUIInsertObject
 - OleUIInsertObjectA
 - OleUIInsertObjectW
---

# OleUIInsertObjectW function


## -description

Invokes the standard <b>Insert Object</b> dialog box, which allows the user to select an object source and class name, as well as the option of displaying the object as itself or as an icon.

## -parameters

### -param unnamedParam1 [in]

 Pointer to the in-out <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiinsertobjecta">OLEUIINSERTOBJECT</a> structure for this dialog box.

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
<dt><b>OLEUI_ERR_STANDARDMAX </b></dt>
</dl>
</td>
<td width="60%">
Errors common to all dialog boxes lie in the range OLEUI_ERR_STANDARDMIN to OLEUI_ERR_STANDARDMAX. This value allows the application to test for standard messages in order to display error messages to the user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_IOERR_LPSZFILEINVALID </b></dt>
</dl>
</td>
<td width="60%">
The <b>lpszFile</b> value is invalid or user has insufficient write access permissions.This <b>lpszFile</b> member points to the name of the file linked to or inserted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_IOERR_PPVOBJINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppvOjb</i> value is invalid. This member points to the location where the pointer for the object is returned. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_IOERR_LPIOLECLIENTSITEINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <b>lpIOleClientSite</b> value is invalid. This member points to the client site for the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_IOERR_LPISTORAGEINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <b>lpIStorage</b> value is invalid. This member points to the storage to be used for the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_IOERR_SCODEHASERROR</b></dt>
</dl>
</td>
<td width="60%">
The <b>sc</b> member of <i>lpIO</i> has additional error information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_IOERR_LPCLSIDEXCLUDEINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <b>lpClsidExclude</b> value is invalid. This member contains the list of CLSIDs to exclude.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_IOERR_CCHFILEINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <b>cchFile</b> or <b>lpszFile</b> value is invalid. The <b>cchFile</b> member specifies the size of the <b>lpszFile</b> buffer. The <b>lpszFile</b> member points to the name of the file linked to or inserted.

</td>
</tr>
</table>

## -remarks

<b>OleUIInsertObject</b> allows the user to select the type of object to be inserted from a list box containing the object applications registered on the user's system. To populate that list box, <b>OleUIInsertObject</b> traverses the registry, adding every object server it finds that meets the following criteria:

<ul>
<li>The registry entry does not include the NotInsertable key.</li>
<li>The registry entry includes an OLE 1.0 style Protocol\\StdFileEditing\\Server key.</li>
<li>The registry entry includes the Insertable key.</li>
<li>The object's CLSID is not included in the list of objects to exclude (the <b>lpClsidExclude</b> member of <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiinsertobjecta">OLEUIINSERTOBJECT</a>).</li>
</ul>
By default, <b>OleUIInsertObject</b> does not validate object servers, however, if the IOF_VERIFYSERVEREXIST flag is included in the dwFlags member of the <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiinsertobjecta">OLEUIINSERTOBJECT</a> structure, <b>OleUIInsertObject</b> verifies that the server exists. If it does not exist, then the server's object is not added to the list of available objects. Server validation is a time-extensive operation and is a significant performance factor.

To free an <b>HMETAFILEPICT</b> returned from the <b>Insert Object</b> or <b>Paste Special</b> dialog box, delete the attached metafile on the handle, as follows:


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
> The oledlg.h header defines OLEUIINSERTOBJECT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuiinsertobjecta">OLEUIINSERTOBJECT</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openfile">OpenFile</a>
