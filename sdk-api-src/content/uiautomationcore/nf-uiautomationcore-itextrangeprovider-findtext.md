---
UID: NF:uiautomationcore.ITextRangeProvider.FindText
title: ITextRangeProvider::FindText
author: windows-sdk-content
description: Returns a text range subset that contains the specified text.
old-location: winauto\uiauto_ITextRangeProvider_FindText.htm
old-project: WinAuto
ms.assetid: 6012bc1e-5c1c-4874-ba2b-5e16eaf21f1d
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: FindText, FindText method [Windows Accessibility], FindText method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],FindText method, ITextRangeProvider.FindText, ITextRangeProvider::FindText, uiauto.uiauto_ITextRangeProvider_FindText, uiauto_ITextRangeProvider_FindText, uiautomationcore/ITextRangeProvider::FindText, winauto.uiauto_ITextRangeProvider_FindText
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.h
api_name:
-	ITextRangeProvider.FindText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRangeProvider::FindText


## -description



        Returns a text range subset that contains the specified text.
        


## -parameters




### -param text [in]

Type: <b>BSTR</b>

The text string to search for.


### -param backward [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the last occurring text range should be returned instead of the first; otherwise <b>FALSE</b>.


### -param ignoreCase [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if case should be ignored; otherwise <b>FALSE</b>.


### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>**</b>

Receives a pointer to the text range
				matching the specified text; otherwise <b>NULL</b>. 
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



There is no differentiation between hidden and visible text.





## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

