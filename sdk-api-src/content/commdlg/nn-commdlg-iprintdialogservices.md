---
UID: NN:commdlg.IPrintDialogServices
title: IPrintDialogServices
author: windows-sdk-content
description: Provides methods that enable an application using the PrintDlgEx function to retrieve information about the currently selected printer.
old-location: dlgbox\iprintdialogservices.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogservices.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IPrintDialogServices, IPrintDialogServices interface [Dialog Boxes], IPrintDialogServices interface [Dialog Boxes],described, _win32_IPrintDialogServices, _win32_iprintdialogservices_cpp, commdlg/IPrintDialogServices, dlgbox.iprintdialogservices, winui._win32_iprintdialogservices
ms.prod: windows
ms.technology: windows-sdk
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


Provides methods that enable an application using the <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> function to retrieve information about the currently selected printer.


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
<a href="https://msdn.microsoft.com/f825a5c4-ecc6-4ec3-8500-33a67891337b">GetCurrentDevMode</a>
</td>
<td align="left" width="63%">
Fills a <a href="https://msdn.microsoft.com/85741025-9393-42ab-8a6d-27f1ae2c0f1b">DEVMODE</a> structure with information about the currently selected printer for use with <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/efd12fd2-2242-4a07-a620-0516ca9e160c">GetCurrentPortName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the current port for use with <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3bd1c1d-b6dc-446b-bb8a-2d8871beccec">GetCurrentPrinterName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the currently selected printer, for use with <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a>.

</td>
</tr>
</table> 


## -remarks



This printer is indicated on the list of installed printers on the <b>General</b> page of the <a href="https://msdn.microsoft.com/b52b71cc-a583-4a21-8a53-501ab442e6f8">Print Property Sheet</a>.



