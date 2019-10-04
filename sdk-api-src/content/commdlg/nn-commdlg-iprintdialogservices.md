---
UID: NN:commdlg.IPrintDialogServices
title: IPrintDialogServices (commdlg.h)
author: windows-sdk-content
description: Provides methods that enable an application using the PrintDlgEx function to retrieve information about the currently selected printer.
old-location: dlgbox\iprintdialogservices.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogservices.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPrintDialogServices, IPrintDialogServices interface [Dialog Boxes], IPrintDialogServices interface [Dialog Boxes],described, _win32_IPrintDialogServices, _win32_iprintdialogservices_cpp, commdlg/IPrintDialogServices, dlgbox.iprintdialogservices, winui._win32_iprintdialogservices
ms.topic: interface
f1_keywords: 
 - "commdlg/IPrintDialogServices"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Comdlg32.dll
api_name:
 - IPrintDialogServices
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPrintDialogServices interface


## -description


Provides methods that enable an application using the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a> function to retrieve information about the currently selected printer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintDialogServices</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPrintDialogServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrintDialogServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/commdlg/nf-commdlg-getcurrentdevmode">GetCurrentDevMode</a>
</td>
<td align="left" width="63%">
Fills a <a href="https://docs.microsoft.com/windows/win32/api/wingdi/ns-wingdi-devmodea">DEVMODE</a> structure with information about the currently selected printer for use with <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/commdlg/nf-commdlg-getcurrentportname">GetCurrentPortName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the current port for use with <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/commdlg/nf-commdlg-getcurrentprintername">GetCurrentPrinterName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the currently selected printer, for use with <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)">PrintDlgEx</a>.

</td>
</tr>
</table> 


## -remarks



This printer is indicated on the list of installed printers on the <b>General</b> page of the <a href="https://docs.microsoft.com/windows/desktop/dlgbox/print-property-sheet">Print Property Sheet</a>.



