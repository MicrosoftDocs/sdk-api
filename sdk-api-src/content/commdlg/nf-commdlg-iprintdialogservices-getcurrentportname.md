---
UID: NF:commdlg.IPrintDialogServices.GetCurrentPortName
title: IPrintDialogServices::GetCurrentPortName (commdlg.h)
description: Retrieves the name of the current port for use with PrintDlgEx.
helpviewer_keywords: ["GetCurrentPortName","GetCurrentPortName function","GetCurrentPortName method [Dialog Boxes]","GetCurrentPortName method [Dialog Boxes]","IPrintDialogServices interface","IPrintDialogServices interface [Dialog Boxes]","GetCurrentPortName method","IPrintDialogServices.GetCurrentPortName","IPrintDialogServices::GetCurrentPortName","_win32_IPrintDialogServices_GetCurrentPortName","_win32_iprintdialogservices_getcurrentportname_cpp","commdlg/IPrintDialogServices::GetCurrentPortName","dlgbox.iprintdialogservices_getcurrentportname","winui._win32_iprintdialogservices_getcurrentportname"]
old-location: dlgbox\iprintdialogservices_getcurrentportname.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogservices\iprintdialogservicesgetcurrentportname.htm
ms.date: 12/05/2018
ms.keywords: GetCurrentPortName, GetCurrentPortName function, GetCurrentPortName method [Dialog Boxes], GetCurrentPortName method [Dialog Boxes],IPrintDialogServices interface, IPrintDialogServices interface [Dialog Boxes],GetCurrentPortName method, IPrintDialogServices.GetCurrentPortName, IPrintDialogServices::GetCurrentPortName, _win32_IPrintDialogServices_GetCurrentPortName, _win32_iprintdialogservices_getcurrentportname_cpp, commdlg/IPrintDialogServices::GetCurrentPortName, dlgbox.iprintdialogservices_getcurrentportname, winui._win32_iprintdialogservices_getcurrentportname
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
 - IPrintDialogServices::GetCurrentPortName
 - commdlg/IPrintDialogServices::GetCurrentPortName
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
 - IPrintDialogServices.GetCurrentPortName
---

# IPrintDialogServices::GetCurrentPortName


## -description

Retrieves the name of the current port for use with <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a>.

## -parameters

### -param pPortName

Type: <b>LPTSTR</b>

The name of the current port.

### -param pcchSize

Type: <b>UINT*</b>

On input, the variable specifies the size, in characters, of the buffer pointed to by the <i>lpPortName</i> parameter. On output, the variable contains the number of bytes (ANSI) or characters (Unicode), including the terminating null character, written to the buffer.

If the size is zero on input, the function returns the required buffer size (in bytes or characters) in <i>pcchSize</i> and does not use the <i>lpPortName</i> buffer.

## -returns

Type: <b>HRESULT</b>

If the method is successful, the return value is <b>S_OK</b>. If there is no current port, the return value is <b>S_OK</b>, the value returned in <i>pcchSize</i> is zero, and the <i>lpPortName</i> buffer is unchanged.

If an error occurs, the return value is a COM error code. For more information, see <a href="/windows/desktop/SetupApi/error-handling">Error Handling</a>.

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogservices">IPrintDialogServices</a>



<a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a>



<b>Reference</b>