---
UID: NF:commdlg.IPrintDialogServices.GetCurrentDevMode
title: IPrintDialogServices::GetCurrentDevMode (commdlg.h)
description: Fills a DEVMODE structure with information about the currently selected printer for use with PrintDlgEx.
helpviewer_keywords: ["GetCurrentDevMode","GetCurrentDevMode function","GetCurrentDevMode method [Dialog Boxes]","GetCurrentDevMode method [Dialog Boxes]","IPrintDialogServices interface","IPrintDialogServices interface [Dialog Boxes]","GetCurrentDevMode method","IPrintDialogServices.GetCurrentDevMode","IPrintDialogServices::GetCurrentDevMode","_win32_IPrintDialogServices_GetCurrentDevMode","_win32_iprintdialogservices_getcurrentdevmode_cpp","commdlg/IPrintDialogServices::GetCurrentDevMode","dlgbox.iprintdialogservices_getcurrentdevmode","winui._win32_iprintdialogservices_getcurrentdevmode"]
old-location: dlgbox\iprintdialogservices_getcurrentdevmode.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogservices\iprintdialogservicesgetcurrentdevmode.htm
ms.date: 12/05/2018
ms.keywords: GetCurrentDevMode, GetCurrentDevMode function, GetCurrentDevMode method [Dialog Boxes], GetCurrentDevMode method [Dialog Boxes],IPrintDialogServices interface, IPrintDialogServices interface [Dialog Boxes],GetCurrentDevMode method, IPrintDialogServices.GetCurrentDevMode, IPrintDialogServices::GetCurrentDevMode, _win32_IPrintDialogServices_GetCurrentDevMode, _win32_iprintdialogservices_getcurrentdevmode_cpp, commdlg/IPrintDialogServices::GetCurrentDevMode, dlgbox.iprintdialogservices_getcurrentdevmode, winui._win32_iprintdialogservices_getcurrentdevmode
req.header: commdlg.h
req.include-header: Windows.h
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
req.lib: 
req.dll: Comdlg32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPrintDialogServices::GetCurrentDevMode
 - commdlg/IPrintDialogServices::GetCurrentDevMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comdlg32.dll
api_name:
 - IPrintDialogServices.GetCurrentDevMode
---

# IPrintDialogServices::GetCurrentDevMode


## -description

Fills a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure with information about the currently selected printer for use with <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a>.

## -parameters

### -param pDevMode

Type: <b>LPDEVMODE</b>

A pointer to a buffer that receives a <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure containing information about the currently selected printer.

### -param pcbSize

Type: <b>UINT*</b>

On input, the variable specifies the size, in bytes, of the buffer pointed to by the <i>lpDevMode</i> parameter. On output, the variable contains the number of bytes written to <i>lpDevMode</i>.

If the size is zero on input, the function returns the required buffer size (in bytes) in <i>pcbSize</i> and does not use the <i>lpDevMode</i> buffer.

## -returns

Type: <b>HRESULT</b>

If the method is successful, the return value is <b>S_OK</b>. If no printer is currently selected, the return value is <b>S_OK</b>, the value returned in <i>pcbSize</i> is zero, and the <i>lpDevMode</i> buffer is unchanged.

If an error occurs, the return value is a COM error code. For more information, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a>



<a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogservices">IPrintDialogServices</a>



<a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a>



<b>Reference</b>