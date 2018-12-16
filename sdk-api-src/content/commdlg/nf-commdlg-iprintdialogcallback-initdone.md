---
UID: NF:commdlg.IPrintDialogCallback.InitDone
title: IPrintDialogCallback::InitDone
author: windows-sdk-content
description: Called by PrintDlgEx when the system has finished initializing the General page of the Print Property Sheet.
old-location: dlgbox\iprintdialogcallback_initdone.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogcallback\iprintdialogcallbackinitdone.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPrintDialogCallback interface [Dialog Boxes],InitDone method, IPrintDialogCallback.InitDone, IPrintDialogCallback::InitDone, InitDone, InitDone method [Dialog Boxes], InitDone method [Dialog Boxes],IPrintDialogCallback interface, _win32_IPrintDialogCallback_InitDone, _win32_iprintdialogcallback_initdone_cpp, commdlg/IPrintDialogCallback::InitDone, dlgbox.iprintdialogcallback_initdone, winui._win32_iprintdialogcallback_initdone
ms.topic: method
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
 - IPrintDialogCallback.InitDone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPrintDialogCallback::InitDone


## -description


Called by <a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a> when the system has finished initializing the <b>General</b> page of the <a href="https://msdn.microsoft.com/en-us/library/ms646966(v=VS.85).aspx">Print Property Sheet</a>.


## -parameters






## -returns



Type: <b>HRESULT</b>

Return <b>S_OK</b> to prevent the <a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a> function from performing its default actions.

Return <b>S_FALSE</b> to allow <a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a> to perform its default actions. Currently, <b>PrintDlgEx</b> does not perform any default processing after the <b>InitDone</b> call.




## -remarks



If your callback object implements the <a href="https://msdn.microsoft.com/en-us/library/ms693765(v=VS.85).aspx">IObjectWithSite</a> interface, the <a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a> function calls the <a href="https://msdn.microsoft.com/library/ms683869(v=VS.85).aspx">IObjectWithSite::SetSite</a> method to pass an <a href="https://msdn.microsoft.com/en-us/library/ms646897(v=VS.85).aspx">IPrintDialogServices</a> pointer to the callback object. The <b>PrintDlgEx</b> function calls the <b>IObjectWithSite::SetSite</b> method before calling the <b>InitDone</b> method. This enables your <b>InitDone</b> implementation to use the <b>IPrintDialogServices</b> methods to retrieve information about the currently selected printer.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms645524(v=VS.85).aspx">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646896(v=VS.85).aspx">IPrintDialogCallback</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646897(v=VS.85).aspx">IPrintDialogServices</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646942(v=VS.85).aspx">PrintDlgEx</a>



<b>Reference</b>
 

 

