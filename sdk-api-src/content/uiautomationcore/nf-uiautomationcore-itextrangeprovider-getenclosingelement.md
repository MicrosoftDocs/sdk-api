---
UID: NF:uiautomationcore.ITextRangeProvider.GetEnclosingElement
title: ITextRangeProvider::GetEnclosingElement
author: windows-sdk-content
description: Returns the innermost element that encloses the text range.
old-location: winauto\uiauto_ITextRangeProvider_GetEnclosingElement.htm
tech.root: WinAuto
ms.assetid: 51615c53-3239-41d6-895b-dbda68b6b4db
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetEnclosingElement, GetEnclosingElement method [Windows Accessibility], GetEnclosingElement method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],GetEnclosingElement method, ITextRangeProvider.GetEnclosingElement, ITextRangeProvider::GetEnclosingElement, uiauto.uiauto_ITextRangeProvider_GetEnclosingElement, uiauto_ITextRangeProvider_GetEnclosingElement, uiautomationcore/ITextRangeProvider::GetEnclosingElement, winauto.uiauto_ITextRangeProvider_GetEnclosingElement
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextRangeProvider.GetEnclosingElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationcore.h
: 
- ITextRangeProvider.GetEnclosingElement
: 
---

# ITextRangeProvider::GetEnclosingElement


## -description


Returns the innermost element that encloses the text range. 


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>**</b>

Receives a pointer to the UI Automation provider of the enclosing element.
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The enclosing element is typically the text provider that supplies the text range. However,
		if the text provider supports child elements such as tables or hyperlinks, 
		the enclosing element could be a descendant of the text provider.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

