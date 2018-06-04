---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# OleUIBusyA function


## -description


Invokes the standard <b>Busy</b> dialog box, allowing the user to manage concurrency.




## -parameters




### -param Arg1

TBD




#### - lpBZ [in]

Pointer to an <a href="https://msdn.microsoft.com/53c30da9-36f3-40f0-8176-15df1a34bdb8">OLEUIBUSY</a> structure that contains information used to initialize the dialog box.


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
The user has pressed <b>Switch To</b> and <a href="https://msdn.microsoft.com/317f0dbf-7ac9-4e5a-a5ed-e6b807f07fb2">OleUIBusy</a> was unable to determine how to switch to the blocking application. In this case, the caller should either take measures to attempt to resolve the conflict itself, if possible, or retry the operation. <b>OleUIBusy</b> will only return OLEUI_BZ_SWITCHTOSELECTED if the user has pressed the <b>Switch To</b> button, <i>hTask</i> is <b>NULL</b> and the BZ_NOTRESPONDING flag is set. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_BZ_SWITCHTOSELECTED</b></dt>
</dl>
</td>
<td width="60%">
The user has pressed <b>Switch To</b> and <a href="https://msdn.microsoft.com/317f0dbf-7ac9-4e5a-a5ed-e6b807f07fb2">OleUIBusy</a> was unable to determine how to switch to the blocking application. In this case, the caller should either take measures to attempt to resolve the conflict itself, if possible, or retry the operation. <b>OleUIBusy</b> will only return OLEUI_BZ_SWITCHTOSELECTED if the user has pressed the <b>Switch To</b> button, <i>hTask</i> is <b>NULL</b> and the BZ_NOTRESPONDING flag is set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLEUI_BZ_SWITCHTOSELECTED</b></dt>
</dl>
</td>
<td width="60%">
The user has pressed <b>Switch To</b> and <a href="https://msdn.microsoft.com/317f0dbf-7ac9-4e5a-a5ed-e6b807f07fb2">OleUIBusy</a> was unable to determine how to switch to the blocking application. In this case, the caller should either take measures to attempt to resolve the conflict itself, if possible, or retry the operation. <b>OleUIBusy</b> will only return OLEUI_BZ_SWITCHTOSELECTED if the user has pressed the <b>Switch To</b> button, <i>hTask</i> is <b>NULL</b> and the BZ_NOTRESPONDING flag is set. 

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
Unable to call <a href="_win32_LoadString_cpp">LoadString</a> for the localized resources from the library.

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
<dt><b>OLEUI_BZERR_HTASKINVALID</b></dt>
</dl>
</td>
<td width="60%">
The hTask specified in the <i>hTask</i> member of the <a href="https://msdn.microsoft.com/53c30da9-36f3-40f0-8176-15df1a34bdb8">OLEUIBUSY</a> structure is invalid.

</td>
</tr>
</table>
 




## -remarks



The standard OLE Server <b>Busy</b> dialog box notifies the user that the server application is not receiving messages. The dialog box then asks the user to cancel the operation, switch to the task that is blocked, or continue waiting.





## -see-also




<a href="https://msdn.microsoft.com/53c30da9-36f3-40f0-8176-15df1a34bdb8">OLEUIBUSY</a>
 

 

