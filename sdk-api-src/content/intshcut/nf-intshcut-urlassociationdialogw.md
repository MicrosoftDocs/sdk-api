---
UID: NF:intshcut.URLAssociationDialogW
title: URLAssociationDialogW function (intshcut.h)
description: Invokes the unregistered URL protocol dialog box. (Unicode)
helpviewer_keywords: ["URLASSOCDLG_FL_REGISTER_ASSOC", "URLASSOCDLG_FL_USE_DEFAULT_NAME", "URLAssociationDialog", "URLAssociationDialog function [Windows Shell]", "URLAssociationDialogW", "_win32_URLAssociationDialog", "intshcut/URLAssociationDialog", "intshcut/URLAssociationDialogW", "shell.URLAssociationDialog"]
old-location: shell\URLAssociationDialog.htm
tech.root: shell
ms.assetid: 3158e819-f131-4f57-8516-998955100377
ms.date: 12/05/2018
ms.keywords: URLASSOCDLG_FL_REGISTER_ASSOC, URLASSOCDLG_FL_USE_DEFAULT_NAME, URLAssociationDialog, URLAssociationDialog function [Windows Shell], URLAssociationDialogA, URLAssociationDialogW, _win32_URLAssociationDialog, intshcut/URLAssociationDialog, intshcut/URLAssociationDialogA, intshcut/URLAssociationDialogW, shell.URLAssociationDialog
req.header: intshcut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: URLAssociationDialogW (Unicode) and URLAssociationDialogA (ANSI)
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
 - URLAssociationDialogW
 - intshcut/URLAssociationDialogW
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
 - URLAssociationDialog
 - URLAssociationDialogA
 - URLAssociationDialogW
---

# URLAssociationDialogW function


## -description

Invokes the unregistered URL protocol dialog box. This dialog box allows the user to select an application to associate with a previously unknown protocol.
<div class="alert"><b>Note</b>  Windows XP Service Pack 2 (SP2) or later: This function is no longer supported.</div><div> </div>

## -parameters

### -param hwndParent

Type: <b>HWND</b>

A handle to the parent window.

### -param dwInFlags

Type: <b>DWORD</b>

The bit flags that specify the behavior of the function. This value can be a combination of the following:



#### URLASSOCDLG_FL_USE_DEFAULT_NAME

Use the default file name (that is, "Internet Shortcut").



#### URLASSOCDLG_FL_REGISTER_ASSOC

Register the selected application as the handler for the protocol specified in <i>pcszURL</i>. The application is registered only if this flag is set and the user indicates that a persistent association is desired.

### -param pcszFile

Type: <b>PTCSTR</b>

The address of a constant zero-terminated string that contains the file name to associate with the URLs protocol.

### -param pcszURL

Type: <b>PTCSTR</b>

The address of a constant zero-terminated string that contains the URL with an unknown protocol.

### -param pszAppBuf [out]

Type: <b>PTSTR</b>

The address of a buffer that receives the path of the application specified by the user.

### -param ucAppBufLen

Type: <b>UINT</b>

The size of <i>pszAppBuf</i>, in characters.


##### - dwInFlags.URLASSOCDLG_FL_REGISTER_ASSOC

Register the selected application as the handler for the protocol specified in <i>pcszURL</i>. The application is registered only if this flag is set and the user indicates that a persistent association is desired.


##### - dwInFlags.URLASSOCDLG_FL_USE_DEFAULT_NAME

Use the default file name (that is, "Internet Shortcut").

## -returns

Type: <b>HRESULT</b>

<div class="alert"><b>Note</b>  As of Windows XP SP2, this function not supported and returns E_NOTIMPL in all situations.</div>
<div> </div>
In supported systems, returns S_OK if the application is registered with the URL protocol, or S_FALSE if nothing is registered. For example, the function returns S_FALSE when the user elects to perform a one-time execution via the selected application.

## -remarks

> [!NOTE]
> The intshcut.h header defines URLAssociationDialog as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

