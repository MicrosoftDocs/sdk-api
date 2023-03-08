---
UID: NF:mergemod.IMsmMerge.OpenModule
title: IMsmMerge::OpenModule (mergemod.h)
description: The OpenModule method opens a Windows Installer merge module in read-only mode. A module must be opened before it can be merged with an installation database. For more information, see the OpenModule method of the Merge object.
helpviewer_keywords: ["IMsmMerge interface","OpenModule method","IMsmMerge.OpenModule","IMsmMerge::OpenModule","OpenModule","OpenModule method","OpenModule method","IMsmMerge interface","_msi_openmodule_function","mergemod/IMsmMerge::OpenModule","setup.imsmmerge_openmodule"]
old-location: setup\imsmmerge_openmodule.htm
tech.root: setup
ms.assetid: 37225e61-c24f-4a44-8fdf-673590a6e09d
ms.date: 12/05/2018
ms.keywords: IMsmMerge interface,OpenModule method, IMsmMerge.OpenModule, IMsmMerge::OpenModule, OpenModule, OpenModule method, OpenModule method,IMsmMerge interface, _msi_openmodule_function, mergemod/IMsmMerge::OpenModule, setup.imsmmerge_openmodule
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.lib: 
req.dll: Mergemod.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMsmMerge::OpenModule
 - mergemod/IMsmMerge::OpenModule
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge.OpenModule
---

# IMsmMerge::OpenModule


## -description

The 
<b>OpenModule</b> method opens a Windows Installer merge module in read-only mode. A module must be opened before it can be merged with an installation database. For more information, see the 
<a href="/windows/desktop/Msi/merge-openmodule">OpenModule</a> method of the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object.  

<b>IMsmMerge2::OpenModule</b>    Mergemod.dll version 2.0 and later.<div> </div><b>IMsmMerge::OpenModule</b>      All Mergemod.dll versions.

## -parameters

### -param Path [in]

Fully qualified file name that points to a merge module. A <b>LPCWSTR</b> can be used in place of a <b>BSTR</b>.

### -param Language [in]

A language identifier (<b>LANGID</b>).

## -returns

The <b>OpenModule</b> function returns the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The file specified is a Windows Installer database, but is not a merge module (missing 
<a href="/windows/desktop/Msi/modulesignature-table">ModuleSignature table</a>).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_LANGUAGE_UNSUPPORTED as HRESULT </b></dt>
</dl>
</td>
<td width="60%">
The language is not supported by the module.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_TRANSFORM_FAILURE as HRESULT</b></dt>
</dl>
</td>
<td width="60%">
The language is supported by the module, but there was an error applying the transform.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPEN_FAILED as HRESULT </b></dt>
</dl>
</td>
<td width="60%">
The file could not be opened as a Windows Installer database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TOO_MANY_OPEN_FILES as HRESULT </b></dt>
</dl>
</td>
<td width="60%">
There is already a module open. Closes the current module first.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>

## -remarks

This function opens the merge module in read-only mode (MSIDBOPEN_READONLY), and excludes other programs from writing to the merge module until the 
<a href="/windows/desktop/Msi/merge-closemodule">CloseModule</a> function is called. A merge module must be opened before it can be merged.

The installer attempts to open the module in the language specified by <i>Language</i> or in any more general language. For example, if 1033 is specified by the <i>Language</i> value, a module with a default language of 1033, 9, or 0 is opened in its default language. A <i>Language</i> value of 9  opens modules with a default language of 9 or 0. If the default language of the module does not meet the specified requirements, an attempt is made to transform the module into the requested language. If that fails, the installer attempts to transform the module into increasingly general languages, all the way to language neutral. If none of the transforms succeed, the module fails to open. In this case, an error is added to the error list of type msmErrorLanguageUnsupported and the function returns ERROR_INSTALL_LANGUAGE_UNSUPPORTED as HRESULT.

If there is an error transforming the module to the desired language, an error is created of type msmErrorLanguageFailed and the function returns ERROR_INSTALL_TRANSFORM_FAILURE as HRESULT.

For more information, see the 
<a href="/windows/desktop/Msi/error-type">Type</a> property of the 
<a href="/windows/desktop/Msi/error-object">Error</a> object.

Opening a merge module clears any errors that have not already been retrieved.

## -see-also

<a href="/windows/desktop/Msi/merge-module-automation">Merge Module Automation</a>