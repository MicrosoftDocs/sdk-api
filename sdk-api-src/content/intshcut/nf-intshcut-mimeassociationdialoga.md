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

# MIMEAssociationDialogA function


## -description


Runs the unregistered MIME content type dialog box.
<div class="alert"><b>Note</b>  Windows XP Service Pack 2 (SP2) or later: This function is no longer supported.</div><div> </div>

## -parameters




### -param hwndParent

Type: <b>HWND</b>

A handle to the parent window of any posted child windows.


### -param dwInFlags

Type: <b>DWORD</b>

A bit flag value that specifies if an association is to be registered. The bit flag is the value MIMEASSOCDLG_FL_REGISTER_ASSOC (0x0001). If this bit is set, the selected application is registered as the handler for the given MIME type. If this bit is clear, no association is registered.

An application is registered only if this flag is set and the user indicates that a persistent association is to be made.

Registration is impossible if the string at <i>pcszFile</i> does not contain an extension.


### -param pcszFile

Type: <b>PCTSTR</b>

The address of a null-terminated string that contains the name of the target file. This file must conform to the content type described by the <i>pcszMIMEContentType</i> parameter.


### -param pcszMIMEContentType

Type: <b>PCTSTR</b>

The address of a null-terminated string that contains the unregistered content type.


### -param pszAppBuf [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the path of the application specified by the user.


### -param ucAppBufLen

Type: <b>UINT</b>

Size of <i>pszAppBuf</i>, in characters.


## -returns



Type: <b>HRESULT</b>

<div class="alert"><b>Note</b>  As of Windows XP SP2, this function is not supported and returns E_NOTIMPL in all situations.</div>
<div> </div>
In supported systems, returns S_OK if the content type was successfully associated with the extension. In this case, the extension is associated as the default for the content type, and <i>pszAppBuf</i> points to the string that contains the path of the specified application. The function returns S_FALSE if nothing was registered. Otherwise, the return value will be one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The user canceled the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The flag combination passed in <i>dwInFlags</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
One of the input pointers is invalid.

</td>
</tr>
</table>
 




## -remarks



This function does not validate the syntax of the input content type string at <i>pcszMIMEContentType</i>. A successful return value does not indicate that the specified MIME content type is valid.



