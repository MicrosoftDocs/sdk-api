---
UID: NN:commdlg.IPrintDialogServices
title: IPrintDialogServices
author: windows-sdk-content
description: Provides methods that enable an application using the PrintDlgEx function to retrieve information about the currently selected printer.
old-location: dlgbox\iprintdialogservices.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogservices.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPrintDialogServices, IPrintDialogServices interface [Dialog Boxes], IPrintDialogServices interface [Dialog Boxes],described, _win32_IPrintDialogServices, _win32_iprintdialogservices_cpp, commdlg/IPrintDialogServices, dlgbox.iprintdialogservices, winui._win32_iprintdialogservices
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrintDialogServices interface


## -description


Provides methods that enable an application using the <a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a> function to retrieve information about the currently selected printer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintDialogServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPrintDialogServices</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms646899(v=VS.85).aspx">GetCurrentDevMode</a>
</td>
<td align="left" width="63%">
Fills a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure with information about the currently selected printer for use with <a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms646900(v=VS.85).aspx">GetCurrentPortName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the current port for use with <a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms646903(v=VS.85).aspx">GetCurrentPrinterName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the currently selected printer, for use with <a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a>.

</td>
</tr>
</table> 


## -remarks



This printer is indicated on the list of installed printers on the <b>General</b> page of the <a href="https://msdn.microsoft.com/en-us/library/ms646966(v=VS.85).aspx">Print Property Sheet</a>.



