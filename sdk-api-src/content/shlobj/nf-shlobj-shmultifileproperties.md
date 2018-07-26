---
UID: NF:shlobj.SHMultiFileProperties
title: SHMultiFileProperties function
author: windows-sdk-content
description: Displays a merged property sheet for a set of files. Property values common to all the files are shown while those that differ display the string (multiple values).
old-location: shell\SHMultiFileProperties.htm
old-project: shell
ms.assetid: 7c66fd91-4f7a-45f3-b849-bf210c552511
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: SHMultiFileProperties, SHMultiFileProperties function [Windows Shell], _win32_SHMultiFileProperties, shell.SHMultiFileProperties, shlobj/SHMultiFileProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHMultiFileProperties
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
---

# SHMultiFileProperties function


## -description


Displays a merged property sheet for a set of files. Property values common to all the files are shown while those that differ display the string <b>(multiple values)</b>.


## -parameters




### -param pdtobj [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to a data object that supplies the PIDLs of all of the files for which to display the merged property sheet. The data object must use the <a href="https://msdn.microsoft.com/fb8ce5d3-3215-4e05-a916-4d4a803464d2">CFSTR_SHELLIDLIST</a> clipboard format. The parent folder's implementation of <a href="https://msdn.microsoft.com/2164bbe6-e030-4a64-85db-9ee1cd3c136d">IShellFolder::GetDisplayNameOf</a> must return a fully qualified file system path for each item in response to the <a href="https://msdn.microsoft.com/5d87609d-bcbf-4a4f-a97e-017ee8a9879e">SHGDN_FORPARSING</a> flag.


### -param dwFlags

Type: <b>DWORD</b>

Reserved. Must be set to 0.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/fb8ce5d3-3215-4e05-a916-4d4a803464d2">Shell Clipboard Formats</a>
 

 

