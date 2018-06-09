---
UID: NF:uiautomationcore.ITextProvider.GetSelection
title: ITextProvider::GetSelection
author: windows-sdk-content
description: Retrieves a collection of text ranges that represents the currently selected text in a text-based control.
old-location: winauto\uiauto_ITextProvider_GetSelection.htm
old-project: WinAuto
ms.assetid: f5c0b2ed-e891-4856-8829-617a69d4708a
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetSelection, GetSelection method [Windows Accessibility], GetSelection method [Windows Accessibility],ITextProvider interface, ITextProvider interface [Windows Accessibility],GetSelection method, ITextProvider.GetSelection, ITextProvider::GetSelection, uiauto.uiauto_ITextProvider_GetSelection, uiauto_ITextProvider_GetSelection, uiautomationcore/ITextProvider::GetSelection, winauto.uiauto_ITextProvider_GetSelection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextProvider.GetSelection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextProvider::GetSelection


## -description



        Retrieves a collection of text ranges that represents the currently selected text in a text-based control.  
        


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives the address of an array of pointers to the <a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a> interfaces of the text ranges,
				one for each selected span of text. This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        For UI Automation providers that support text selection, 
        the provider should implement this method and also return a <a href="https://msdn.microsoft.com/a1f91515-2bc8-4560-850d-34c880c78c43">ITextProvider::SupportedTextSelection</a> value.
        

If the control contains only a single span of selected text, the <i>pRetVal</i> array should contain a single text range. 

If the control contains a text insertion point but no text is selected,  the <i>pRetVal</i> array should contain a degenerate (empty) text range at the position of the text insertion point.

 If the control contains no selected text, or if the control does not contain a text insertion point, set <i>pRetVal</i> to <b>NULL</b>.
				




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

