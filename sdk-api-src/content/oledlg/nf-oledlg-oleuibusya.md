---
UID: NF:oledlg.OleUIBusyA
title: OleUIBusyA function (oledlg.h)
description: Invokes the standard Busy dialog box, allowing the user to manage concurrency. (ANSI)
helpviewer_keywords: ["OleUIBusyA", "oledlg/OleUIBusyA"]
old-location: com\oleuibusy.htm
tech.root: com
ms.assetid: 317f0dbf-7ac9-4e5a-a5ed-e6b807f07fb2
ms.date: 12/05/2018
ms.keywords: OleUIBusy, OleUIBusy function [COM], OleUIBusyA, OleUIBusyW, _ole_OleUIBusy, com.oleuibusy, oledlg/OleUIBusy, oledlg/OleUIBusyA, oledlg/OleUIBusyW
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OleUIBusyW (Unicode) and OleUIBusyA (ANSI)
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
 - OleUIBusyA
 - oledlg/OleUIBusyA
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
 - OleUIBusy
 - OleUIBusyA
 - OleUIBusyW
---

# OleUIBusyA function


## -description

Invokes the standard <b>Busy</b> dialog box, allowing the user to manage concurrency.

## -parameters

### -param unnamedParam1 [in]

Pointer to an <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuibusya">OLEUIBUSY</a> structure that contains information used to initialize the dialog box.

## -returns

This function returns the following values:


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
<dt><b>OLEUI_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
The user has pressed the <b>Cancel</b> button and that the caller should cancel the operation. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_BZ_SWITCHTOSELECTED</b></dt>
</dl>
</td>
<td width="60%">
The user has pressed <b>Switch To</b> and <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuibusya">OleUIBusy</a> was unable to determine how to switch to the blocking application. In this case, the caller should either take measures to attempt to resolve the conflict itself, if possible, or retry the operation. <b>OleUIBusy</b> will only return OLEUI_BZ_SWITCHTOSELECTED if the user has pressed the <b>Switch To</b> button, <i>hTask</i> is <b>NULL</b> and the BZ_NOTRESPONDING flag is set. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_BZ_SWITCHTOSELECTED</b></dt>
</dl>
</td>
<td width="60%">
The user has pressed <b>Switch To</b> and <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuibusya">OleUIBusy</a> was unable to determine how to switch to the blocking application. In this case, the caller should either take measures to attempt to resolve the conflict itself, if possible, or retry the operation. <b>OleUIBusy</b> will only return OLEUI_BZ_SWITCHTOSELECTED if the user has pressed the <b>Switch To</b> button, <i>hTask</i> is <b>NULL</b> and the BZ_NOTRESPONDING flag is set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_BZ_SWITCHTOSELECTED</b></dt>
</dl>
</td>
<td width="60%">
The user has pressed <b>Switch To</b> and <a href="/windows/desktop/api/oledlg/nf-oledlg-oleuibusya">OleUIBusy</a> was unable to determine how to switch to the blocking application. In this case, the caller should either take measures to attempt to resolve the conflict itself, if possible, or retry the operation. <b>OleUIBusy</b> will only return OLEUI_BZ_SWITCHTOSELECTED if the user has pressed the <b>Switch To</b> button, <i>hTask</i> is <b>NULL</b> and the BZ_NOTRESPONDING flag is set. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_BZ_RETRYSELECTED </b></dt>
</dl>
</td>
<td width="60%">
The user has either pressed the <b>Retry</b> button or attempted to resolve the conflict (probably by switching to the blocking application). In this case, the caller should retry the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_BZ_CALLUNBLOCKED </b></dt>
</dl>
</td>
<td width="60%">
The dialog box has been informed that the operation is no longer blocked. 

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
<dt><b>OLEUI_ERR_CBSTRUCTINCORRECT </b></dt>
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
Unable to call <a href="/windows/desktop/api/winuser/nf-winuser-loadstringa">LoadString</a> for the localized resources from the library.

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
<dt><b>OLEUI_BZERR_HTASKINVALID</b></dt>
</dl>
</td>
<td width="60%">
The hTask specified in the <i>hTask</i> member of the <a href="/windows/desktop/api/oledlg/ns-oledlg-oleuibusya">OLEUIBUSY</a> structure is invalid.

</td>
</tr>
</table>

## -remarks

The standard OLE Server <b>Busy</b> dialog box notifies the user that the server application is not receiving messages. The dialog box then asks the user to cancel the operation, switch to the task that is blocked, or continue waiting.






> [!NOTE]
> The oledlg.h header defines OLEUIBUSY as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/oledlg/ns-oledlg-oleuibusya">OLEUIBUSY</a>
