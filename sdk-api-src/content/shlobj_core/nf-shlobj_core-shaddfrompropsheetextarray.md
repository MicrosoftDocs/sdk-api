---
UID: NF:shlobj_core.SHAddFromPropSheetExtArray
title: SHAddFromPropSheetExtArray function (shlobj_core.h)
description: Adds pages to a property sheet extension array created by SHCreatePropSheetExtArray.
helpviewer_keywords: ["SHAddFromPropSheetExtArray","SHAddFromPropSheetExtArray function [Windows Shell]","_win32_SHAddFromPropSheetExtArray","shell.SHAddFromPropSheetExtArray","shlobj_core/SHAddFromPropSheetExtArray"]
old-location: shell\SHAddFromPropSheetExtArray.htm
tech.root: shell
ms.assetid: e0570cd6-dda2-43e4-8540-58baef37bf18
ms.date: 12/05/2018
ms.keywords: SHAddFromPropSheetExtArray, SHAddFromPropSheetExtArray function [Windows Shell], _win32_SHAddFromPropSheetExtArray, shell.SHAddFromPropSheetExtArray, shlobj_core/SHAddFromPropSheetExtArray
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHAddFromPropSheetExtArray
 - shlobj_core/SHAddFromPropSheetExtArray
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
 - SHAddFromPropSheetExtArray
---

# SHAddFromPropSheetExtArray function


## -description

<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows.]

Adds pages to a property sheet extension array created by <a href="/windows/desktop/api/shlobj/nf-shlobj-shcreatepropsheetextarray">SHCreatePropSheetExtArray</a>.

## -parameters

### -param hpsxa [in]

Type: <b>HPSXA</b>

The array of property sheet handlers returned by <a href="/windows/desktop/api/shlobj/nf-shlobj-shcreatepropsheetextarray">SHCreatePropSheetExtArray</a>.

### -param lpfnAddPage [in]

Type: <b>LPFNADDPROPSHEETPAGE</b>

A pointer to an <a href="/windows/desktop/api/prsht/nc-prsht-lpfnaddpropsheetpage">AddPropSheetPageProc</a> callback function. It is called once for each property sheet handler. The callback function then returns the information needed to add a page to the handler's property sheet.

### -param lParam

Type: <b>LPARAM</b>

A pointer to application-defined data. This data is passed to the callback function specified by <i>lpfnAddPage</i>.

## -returns

Type: <b>UINT</b>

Returns the number of pages actually added.

## -remarks

This function should be called only once for the property sheet extension array named in <i>hpsxa</i>.

This function calls each extension's <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages">IShellPropSheetExt::AddPages</a> method. See that page for further details.

## -see-also

<a href="/windows/desktop/api/shlobj/nf-shlobj-shcreatepropsheetextarray">SHCreatePropSheetExtArray</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shdestroypropsheetextarray">SHDestroyPropSheetExtArray</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shreplacefrompropsheetextarray">SHReplaceFromPropSheetExtArray</a>