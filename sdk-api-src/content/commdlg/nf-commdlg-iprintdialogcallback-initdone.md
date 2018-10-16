---
UID: NF:commdlg.IPrintDialogCallback.InitDone
title: IPrintDialogCallback::InitDone
author: windows-sdk-content
description: Called by PrintDlgEx when the system has finished initializing the General page of the Print Property Sheet.
old-location: dlgbox\iprintdialogcallback_initdone.htm
tech.root: dlgbox
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\commondialogboxlibrary\commondialogboxreference\commondialogboxinterfaces\iprintdialogcallback\iprintdialogcallbackinitdone.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IPrintDialogCallback interface [Dialog Boxes],InitDone method, IPrintDialogCallback.InitDone, IPrintDialogCallback::InitDone, InitDone, InitDone method [Dialog Boxes], InitDone method [Dialog Boxes],IPrintDialogCallback interface, _win32_IPrintDialogCallback_InitDone, _win32_iprintdialogcallback_initdone_cpp, commdlg/IPrintDialogCallback::InitDone, dlgbox.iprintdialogcallback_initdone, winui._win32_iprintdialogcallback_initdone
ms.prod: windows-hardware
ms.technology: windows-devices
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


Called by <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> when the system has finished initializing the <b>General</b> page of the <a href="https://msdn.microsoft.com/b52b71cc-a583-4a21-8a53-501ab442e6f8">Print Property Sheet</a>.


## -parameters






## -returns



Type: <b>HRESULT</b>

Return <b>S_OK</b> to prevent the <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> function from performing its default actions.

Return <b>S_FALSE</b> to allow <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> to perform its default actions. Currently, <b>PrintDlgEx</b> does not perform any default processing after the <b>InitDone</b> call.




## -remarks



If your callback object implements the <a href="_ole_IObjectWithSite">IObjectWithSite</a> interface, the <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> function calls the <a href="_ole_IObjectWithSite_SetSite">IObjectWithSite::SetSite</a> method to pass an <a href="https://msdn.microsoft.com/f8572f39-bccd-40ed-b556-3cac19920f15">IPrintDialogServices</a> pointer to the callback object. The <b>PrintDlgEx</b> function calls the <b>IObjectWithSite::SetSite</b> method before calling the <b>InitDone</b> method. This enables your <b>InitDone</b> implementation to use the <b>IPrintDialogServices</b> methods to retrieve information about the currently selected printer.




## -see-also




<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/51902f34-d0ab-4b49-9302-a8e6e9bd7061">IPrintDialogCallback</a>



<a href="https://msdn.microsoft.com/f8572f39-bccd-40ed-b556-3cac19920f15">IPrintDialogServices</a>



<a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a>



<b>Reference</b>
 

 

