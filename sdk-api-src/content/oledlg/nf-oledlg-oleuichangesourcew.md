---
UID: NF:oledlg.OleUIChangeSourceW
title: OleUIChangeSourceW function
author: windows-sdk-content
description: Invokes the Change Source dialog box, allowing the user to change the source of a link.
old-location: com\oleuichangesource.htm
tech.root: com
ms.assetid: 53ff17aa-3135-462e-885d-3bfbb74ed1c5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OleUIChangeSource, OleUIChangeSource function [COM], OleUIChangeSourceA, OleUIChangeSourceW, _ole_OleUIChangeSource, com.oleuichangesource, oledlg/OleUIChangeSource, oledlg/OleUIChangeSourceA, oledlg/OleUIChangeSourceW
ms.topic: function
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OleUIChangeSourceW (Unicode) and OleUIChangeSourceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleDlg.lib
req.dll: OleDlg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleDlg.dll
api_name:
 - OleUIChangeSource
 - OleUIChangeSourceA
 - OleUIChangeSourceW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OleUIChangeSourceW function


## -description


Invokes the <b>Change Source</b> dialog box, allowing the user to change the source of a link. 




## -parameters




### -param Arg1 [in]

Pointer to the in-out <a href="https://msdn.microsoft.com/440d120c-a121-471b-bee1-f23af136a664">OLEUICHANGESOURCE</a> structure for this dialog box.


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
A call to <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> or the standard <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> allocator failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_ERR_GLOBALMEMALLOC</b></dt>
</dl>
</td>
<td width="60%">
A call to <a href="https://msdn.microsoft.com/06886545-bd5c-4d81-b1c3-dfa7e146e43a">GlobalAlloc</a> or the standard <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> allocator failed.

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
A call to the standard <a href="https://msdn.microsoft.com/047f281e-2665-4d6d-9a0b-918cd3339447">IMalloc</a> allocator failed.

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
<dt><b>OLEUI_CSERR_LINKCNTRNULL</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpOleUILinkContainer</i> value is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_CSERR_LINKCNTRINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpOleUILinkContainer</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_CSERR_FROMNOTNULL</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpszFrom</i> value is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_CSERR_TONOTNULL</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpszTo</i> value is not <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_CSERR_SOURCEINVALID</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpszDisplayName</i> or <i>nFileLength</i> value is invalid, or cannot retrieve the link source.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_CSERR_SOURCEPARSEERROR</b></dt>
</dl>
</td>
<td width="60%">
The <i>nFilename</i> value is wrong.

</td>
</tr>
</table>
 




## -remarks



The link source is not changed by the <b>Change Source</b> dialog box itself. Instead, it is up to the caller to change the link source using the returned file and item strings. The <b>Edit Links</b> dialog box typically does this for the caller. 





## -see-also




<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>



<a href="https://msdn.microsoft.com/440d120c-a121-471b-bee1-f23af136a664">OLEUICHANGESOURCE</a>



<a href="https://msdn.microsoft.com/17c7daf8-83bf-4cfd-a67c-a638630ca263">OleUIEditLinks</a>
 

 

