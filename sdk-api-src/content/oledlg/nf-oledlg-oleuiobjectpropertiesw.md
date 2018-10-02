---
UID: NF:oledlg.OleUIObjectPropertiesW
title: OleUIObjectPropertiesW function
author: windows-sdk-content
description: Invokes the Object Properties dialog box, which displays General, View, and Link information about an object.
old-location: com\oleuiobjectproperties.htm
tech.root: com
ms.assetid: 591f6056-2e5f-4e58-8806-9a0093de2463
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: OleUIObjectProperties, OleUIObjectProperties function [COM], OleUIObjectPropertiesA, OleUIObjectPropertiesW, _ole_OleUIObjectProperties, com.oleuiobjectproperties, oledlg/OleUIObjectProperties, oledlg/OleUIObjectPropertiesA, oledlg/OleUIObjectPropertiesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OleUIObjectPropertiesW function


## -description


Invokes the <b>Object Properties</b> dialog box, which displays <b>General</b>, <b>View</b>, and <b>Link</b> information about an object.




## -parameters




### -param Arg1 [in]

Pointer to the <a href="https://msdn.microsoft.com/7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3">OLEUIOBJECTPROPS</a> structure.


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



<b>OleUIObjectProperties</b> is passed an <a href="https://msdn.microsoft.com/7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3">OLEUIOBJECTPROPS</a> structure, which supplies the information needed to fill in the <b>General</b>, <b>View</b>, and <b>Link</b> tabs of the <b>Object Properties</b> dialog box.




## -see-also




<a href="https://msdn.microsoft.com/aadac00b-47bb-42eb-8458-b23867f6b975">IOleUILinkInfo</a>



<a href="https://msdn.microsoft.com/508dccb3-e98b-4f62-8bc3-98ca2b0d1349">IOleUIObjInfo</a>



<a href="https://msdn.microsoft.com/851d66c8-94a7-47ab-95f4-12a34897de20">OLEUIGNRLPROPS</a>



<a href="https://msdn.microsoft.com/3f355ce8-adc3-4878-a8b4-3f7d94547ef1">OLEUILINKPROPS</a>



<a href="https://msdn.microsoft.com/7a6216d6-061f-48c3-8e3f-5f3e5a63ffb3">OLEUIOBJECTPROPS</a>



<a href="https://msdn.microsoft.com/e45565c5-185e-4143-a5c2-d0b273b5086e">OLEUIVIEWPROPS</a>
 

 

