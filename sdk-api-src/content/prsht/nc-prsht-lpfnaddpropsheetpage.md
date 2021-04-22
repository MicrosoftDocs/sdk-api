---
UID: NC:prsht.LPFNADDPROPSHEETPAGE
title: LPFNADDPROPSHEETPAGE (prsht.h)
description: Specifies an application-defined callback function that a property sheet extension uses to add a page to a property sheet.
helpviewer_keywords: ["AddPropSheetPageProc","AddPropSheetPageProc callback","AddPropSheetPageProc callback function [Windows Controls]","LPFNADDPROPSHEETPAGE","_win32_AddPropSheetPageProc","_win32_AddPropSheetPageProc_cpp","controls.AddPropSheetPageProc","controls._win32_AddPropSheetPageProc","prsht/AddPropSheetPageProc","prsht/LPFNADDPROPSHEETPAGE"]
old-location: controls\AddPropSheetPageProc.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\propsheet\functions\addpropsheetpageproc.htm
ms.date: 12/05/2018
ms.keywords: AddPropSheetPageProc, AddPropSheetPageProc callback, AddPropSheetPageProc callback function [Windows Controls], LPFNADDPROPSHEETPAGE, _win32_AddPropSheetPageProc, _win32_AddPropSheetPageProc_cpp, controls.AddPropSheetPageProc, controls._win32_AddPropSheetPageProc, prsht/AddPropSheetPageProc, prsht/LPFNADDPROPSHEETPAGE
req.header: prsht.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPFNADDPROPSHEETPAGE
 - prsht/LPFNADDPROPSHEETPAGE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Prsht.h
api_name:
 - AddPropSheetPageProc
 - LPFNADDPROPSHEETPAGE
---

# LPFNADDPROPSHEETPAGE callback function


## -description

Specifies an application-defined callback function that a property sheet extension uses to add a page to a property sheet.

## -parameters

### -param unnamedParam1

Type: <b>HPROPSHEETPAGE</b>

Handle to a property sheet page. This parameter is typically called *hPage*.

### -param unnamedParam2

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

Application-defined 32-bit value. This parameter is typically called *lParam*.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.

## -remarks

<div class="alert"><b>Note</b>  This function is not supported when using the Aero wizard style (<a href="/windows/win32/controls/pss-propsheetheader">PSH_AEROWIZARD</a>).</div>
<div> </div>