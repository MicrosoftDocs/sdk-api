---
UID: NF:commdlg.IPrintDialogCallback.InitDone
title: IPrintDialogCallback::InitDone (commdlg.h)
description: Called by PrintDlgEx when the system has finished initializing the General page of the Print Property Sheet.
helpviewer_keywords: ["IPrintDialogCallback interface [Dialog Boxes]","InitDone method","IPrintDialogCallback.InitDone","IPrintDialogCallback::InitDone","InitDone","InitDone method [Dialog Boxes]","InitDone method [Dialog Boxes]","IPrintDialogCallback interface","_win32_IPrintDialogCallback_InitDone","_win32_iprintdialogcallback_initdone_cpp","commdlg/IPrintDialogCallback::InitDone","dlgbox.iprintdialogcallback_initdone","winui._win32_iprintdialogcallback_initdone"]
old-location: dlgbox\iprintdialogcallback_initdone.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogcallback\iprintdialogcallbackinitdone.htm
ms.date: 12/05/2018
ms.keywords: IPrintDialogCallback interface [Dialog Boxes],InitDone method, IPrintDialogCallback.InitDone, IPrintDialogCallback::InitDone, InitDone, InitDone method [Dialog Boxes], InitDone method [Dialog Boxes],IPrintDialogCallback interface, _win32_IPrintDialogCallback_InitDone, _win32_iprintdialogcallback_initdone_cpp, commdlg/IPrintDialogCallback::InitDone, dlgbox.iprintdialogcallback_initdone, winui._win32_iprintdialogcallback_initdone
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
 - commdlg/IPrintDialogCallback.InitDone
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
 - IPrintDialogCallback.InitDone
---

# IPrintDialogCallback::InitDone

## -description

Called by <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> when the system has finished initializing the <b>General</b> page of the <a href="/windows/desktop/dlgbox/print-property-sheet">Print Property Sheet</a>.



## -returns

Type: <b>HRESULT</b>

Return <b>S_OK</b> to prevent the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function from performing its default actions.

Return <b>S_FALSE</b> to allow <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> to perform its default actions. Currently, <b>PrintDlgEx</b> does not perform any default processing after the <b>InitDone</b> call.

## -remarks

If your callback object implements the <a href="/windows/desktop/api/ocidl/nn-ocidl-iobjectwithsite">IObjectWithSite</a> interface, the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function calls the <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">IObjectWithSite::SetSite</a> method to pass an <a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogservices">IPrintDialogServices</a> pointer to the callback object. The <b>PrintDlgEx</b> function calls the <b>IObjectWithSite::SetSite</b> method before calling the <b>InitDone</b> method. This enables your <b>InitDone</b> implementation to use the <b>IPrintDialogServices</b> methods to retrieve information about the currently selected printer.

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogcallback">IPrintDialogCallback</a>



<a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogservices">IPrintDialogServices</a>



<a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a>



<b>Reference</b>
