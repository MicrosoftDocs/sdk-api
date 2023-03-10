---
UID: NF:commdlg.IPrintDialogCallback.SelectionChange
title: IPrintDialogCallback::SelectionChange (commdlg.h)
description: Called by PrintDlgEx when the user selects a different printer from the list of installed printers on the General page of the Print Property Sheet.
helpviewer_keywords: ["IPrintDialogCallback interface [Dialog Boxes]","SelectionChange method","IPrintDialogCallback.SelectionChange","IPrintDialogCallback::SelectionChange","SelectionChange","SelectionChange method [Dialog Boxes]","SelectionChange method [Dialog Boxes]","IPrintDialogCallback interface","_win32_IPrintDialogCallback_SelectionChange","_win32_iprintdialogcallback_selectionchange_cpp","commdlg/IPrintDialogCallback::SelectionChange","dlgbox.iprintdialogcallback_selectionchange","winui._win32_iprintdialogcallback_selectionchange"]
old-location: dlgbox\iprintdialogcallback_selectionchange.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogcallback\iprintdialogcallbackselectionchange.htm
ms.date: 12/05/2018
ms.keywords: IPrintDialogCallback interface [Dialog Boxes],SelectionChange method, IPrintDialogCallback.SelectionChange, IPrintDialogCallback::SelectionChange, SelectionChange, SelectionChange method [Dialog Boxes], SelectionChange method [Dialog Boxes],IPrintDialogCallback interface, _win32_IPrintDialogCallback_SelectionChange, _win32_iprintdialogcallback_selectionchange_cpp, commdlg/IPrintDialogCallback::SelectionChange, dlgbox.iprintdialogcallback_selectionchange, winui._win32_iprintdialogcallback_selectionchange
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
 - commdlg/IPrintDialogCallback.SelectionChange
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
 - IPrintDialogCallback.SelectionChange
---

# IPrintDialogCallback::SelectionChange

## -description

Called by <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> when the user selects a different printer from the list of installed printers on the <b>General</b> page of the <a href="/windows/desktop/dlgbox/print-property-sheet">Print Property Sheet</a>.



## -returns

Type: <b>HRESULT</b>

Return <b>S_OK</b> to prevent the <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function from performing its default actions.

Return <b>S_FALSE</b> to allow <a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> to perform its default actions, which include adjustments to the <b>Copies</b>, <b>Collate</b>, and <b>Print Range</b> items.

## -see-also

<a href="/windows/desktop/dlgbox/common-dialog-box-library">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/commdlg/nn-commdlg-iprintdialogcallback">IPrintDialogCallback</a>



<a href="/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a>



<b>Reference</b>
