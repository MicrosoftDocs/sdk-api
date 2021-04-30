---
UID: NF:muiload.FreeMUILibrary
title: FreeMUILibrary function (muiload.h)
description: Releases the handle to a resource module loaded by LoadMUILibrary.
helpviewer_keywords: ["FreeMUILibrary","FreeMUILibrary function [Internationalization for Windows Applications]","_win32_FreeMUILibrary","intl.freemuilibrary","muiload/FreeMUILibrary"]
old-location: intl\freemuilibrary.htm
tech.root: Intl
ms.assetid: 38a0d7cb-46a9-449b-8f7e-4c573e400e75
ms.date: 12/05/2018
ms.keywords: FreeMUILibrary, FreeMUILibrary function [Internationalization for Windows Applications], _win32_FreeMUILibrary, intl.freemuilibrary, muiload/FreeMUILibrary
req.header: muiload.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Muiload.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Muiload.lib, included in theWindows SDKforWindows VistaonWindows 2000 Professional,Windows Me/98/95.  Not supported onWindows NT 4.0
ms.custom: 19H1
f1_keywords:
 - FreeMUILibrary
 - muiload/FreeMUILibrary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Muiload.lib
api_name:
 - FreeMUILibrary
---

# FreeMUILibrary function


## -description

Releases the handle to a resource module loaded by <a href="/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya">LoadMUILibrary</a>.

## -parameters

### -param hResModule [in]

Handle to a resource module loaded by <a href="/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya">LoadMUILibrary</a>. The handle indicates either a language-specific resource file or an LN file.

## -returns

Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The error code is the same as that returned by <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a>.

## -remarks

Once the application has called <b>FreeMUILibrary</b>, it should treat the passed module handle as invalid.

Applications using this function can be built on pre-Windows Vista operating systems, but they must link statically with the MUILoad library provided in the Microsoft Windows SDK for Windows Vista.

<b>FreeMUILibrary</b> is related to <a href="/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya">LoadMUILibrary</a> in the same way that <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a> is related to <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a>, and similar considerations need to be applied to its usage. In particular, to support correct reference counting, <b>FreeMUILibrary</b> should be called for any handle returned by <b>LoadMUILibrary</b>. For more information see the Remarks sections of <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary">FreeLibrary</a>.

## -see-also

<a href="/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya">LoadMUILibrary</a>



<a href="/windows/desktop/Intl/multilingual-user-interface">Multilingual User Interface</a>



<a href="/windows/desktop/Intl/multilingual-user-interface-functions">Multilingual User Interface Functions</a>