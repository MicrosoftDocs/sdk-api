---
UID: NF:shlobj.SHCreatePropSheetExtArray
title: SHCreatePropSheetExtArray function (shlobj.h)
description: SHCreatePropSheetExtArray may be altered or unavailable.
helpviewer_keywords: ["SHCreatePropSheetExtArray","SHCreatePropSheetExtArray function [Windows Shell]","_win32_SHCreatePropSheetExtArray","shell.SHCreatePropSheetExtArray","shlobj/SHCreatePropSheetExtArray"]
old-location: shell\SHCreatePropSheetExtArray.htm
tech.root: shell
ms.assetid: 88a72529-325d-431e-bc26-bddca787e62b
ms.date: 12/05/2018
ms.keywords: SHCreatePropSheetExtArray, SHCreatePropSheetExtArray function [Windows Shell], _win32_SHCreatePropSheetExtArray, shell.SHCreatePropSheetExtArray, shlobj/SHCreatePropSheetExtArray
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHCreatePropSheetExtArray
 - shlobj/SHCreatePropSheetExtArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHCreatePropSheetExtArray
---

# SHCreatePropSheetExtArray function


## -description

<p class="CCE_Message">[<b>SHCreatePropSheetExtArray</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Loads all the Shell <a href="/previous-versions/windows/desktop/legacy/cc144106(v=vs.85)">property sheet extension handlers</a> located under a specified registry key.

## -parameters

### -param hKey [in]

Type: <b>HKEY</b>

The registry root key that contains the subkey with the property sheet extension handlers. For instance, <b>HKEY_LOCAL_MACHINE</b>.

### -param pszSubKey [in, optional]

Type: <b>PCWSTR</b>

A pointer to a null-terminated string specifying the name of the subkey that contains <b>shellex</b>&#92;<b>PropertySheetHandlers</b>.

For example, if  <i>hkey</i> specifies HKEY_LOCAL_MACHINE and <i>pszSubkey</i> specifies "Software\Microsoft\Windows\CurrentVersion\Controls Folder\Display", this function returns property sheet extension handlers using the following subkey:


<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>Controls Folder</b>
                  <b>Display</b>
                     <b>shellex</b>
                        <b>PropertySheetHandlers</b></pre>

### -param max_iface

Type: <b>UINT</b>

The maximum number of property sheet handlers to be returned.

## -returns

Type: <b>HPSXA</b>

Returns a handle to an array of property sheet handlers. Pass this value to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddfrompropsheetextarray">SHAddFromPropSheetExtArray</a>. You do not access this value directly.

## -remarks

When you are finished with the returned HPSXA handle, destroy it by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdestroypropsheetextarray">SHDestroyPropSheetExtArray</a>.

This function loads up to <i>max_iface</i> property sheet extensions into an array that is then passed to <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddfrompropsheetextarray">SHAddFromPropSheetExtArray</a>.
