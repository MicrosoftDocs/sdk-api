---
UID: NN:commdlg.IPrintDialogCallback
title: IPrintDialogCallback
author: windows-sdk-content
description: Provides methods that enable an application to receive notifications and messages from the PrintDlgEx function while the Print Property Sheet is displayed.
old-location: dlgbox\iprintdialogcallback.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogcallback.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IPrintDialogCallback, IPrintDialogCallback interface [Dialog Boxes], IPrintDialogCallback interface [Dialog Boxes],described, _win32_IPrintDialogCallback, _win32_iprintdialogcallback_cpp, commdlg/IPrintDialogCallback, dlgbox.iprintdialogcallback, winui._win32_iprintdialogcallback
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
 - IPrintDialogCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrintDialogCallback interface


## -description


Provides methods that enable an application to receive notifications and messages from the <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> function while the <a href="https://msdn.microsoft.com/b52b71cc-a583-4a21-8a53-501ab442e6f8">Print Property Sheet</a> is displayed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPrintDialogCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPrintDialogCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPrintDialogCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40b58856-2155-4855-a47d-e6fe1ef7054e">HandleMessage</a>
</td>
<td align="left" width="63%">
Called by <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> to give your application an opportunity to handle messages sent to the child dialog box in the lower portion of the <b>General</b> page of the <a href="https://msdn.microsoft.com/b52b71cc-a583-4a21-8a53-501ab442e6f8">Print Property Sheet</a>. The child dialog box contains controls similar to those of the <b>Print</b> dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b392d3d9-8209-4c31-9500-3104d831ae68">InitDone</a>
</td>
<td align="left" width="63%">
Called by <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> when the system has finished initializing the <b>General</b> page of the <a href="https://msdn.microsoft.com/b52b71cc-a583-4a21-8a53-501ab442e6f8">Print Property Sheet</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0860609-921f-4016-9886-8d150de2634e">SelectionChange</a>
</td>
<td align="left" width="63%">
Called by <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> when the user selects a different printer from the list of installed printers on the <b>General</b> page of the <a href="https://msdn.microsoft.com/b52b71cc-a583-4a21-8a53-501ab442e6f8">Print Property Sheet</a>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f8572f39-bccd-40ed-b556-3cac19920f15">IPrintDialogServices</a>



<a href="https://msdn.microsoft.com/e843d2fc-d122-4112-bfc9-9bfb26e865da">PRINTDLGEX</a>



<a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a>



<b>Reference</b>
 

 

