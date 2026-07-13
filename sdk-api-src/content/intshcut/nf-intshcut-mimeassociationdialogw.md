---
UID: NF:intshcut.MIMEAssociationDialogW
title: MIMEAssociationDialogW function (intshcut.h)
description: Runs the unregistered MIME content type dialog box.Note  Windows XP Service Pack 2 (SP2) or later:\_This function is no longer supported. (Unicode)
helpviewer_keywords: ["MIMEAssociationDialog", "MIMEAssociationDialog function [Windows Shell]", "MIMEAssociationDialogW", "_win32_MIMEAssociationDialog", "intshcut/MIMEAssociationDialog", "intshcut/MIMEAssociationDialogW", "shell.MIMEAssociationDialog"]
old-location: shell\MIMEAssociationDialog.htm
tech.root: shell
ms.assetid: 0f8ee95a-3f95-47ee-822b-740ba134cd3c
ms.date: 12/05/2018
ms.keywords: MIMEAssociationDialog, MIMEAssociationDialog function [Windows Shell], MIMEAssociationDialogA, MIMEAssociationDialogW, _win32_MIMEAssociationDialog, intshcut/MIMEAssociationDialog, intshcut/MIMEAssociationDialogA, intshcut/MIMEAssociationDialogW, shell.MIMEAssociationDialog
req.header: intshcut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MIMEAssociationDialogW (Unicode) and MIMEAssociationDialogA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Url.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MIMEAssociationDialogW
 - intshcut/MIMEAssociationDialogW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Url.dll
api_name:
 - MIMEAssociationDialog
 - MIMEAssociationDialogA
 - MIMEAssociationDialogW
---

# MIMEAssociationDialogW function


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




> [!NOTE]
> The intshcut.h header defines MIMEAssociationDialog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

