---
UID: NF:uiautomationcore.ITextRangeProvider.GetChildren
title: ITextRangeProvider::GetChildren
author: windows-sdk-content
description: Retrieves a collection of all embedded objects that fall within the text range.
old-location: winauto\uiauto_ITextRangeProvider_GetChildren.htm
tech.root: WinAuto
ms.assetid: 2b68a7eb-8ff5-4e8c-830b-e180b2c08be4
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetChildren, GetChildren method [Windows Accessibility], GetChildren method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],GetChildren method, ITextRangeProvider.GetChildren, ITextRangeProvider::GetChildren, uiauto.uiauto_ITextRangeProvider_GetChildren, uiauto_ITextRangeProvider_GetChildren, uiautomationcore/ITextRangeProvider::GetChildren, winauto.uiauto_ITextRangeProvider_GetChildren
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
 - ITextRangeProvider.GetChildren
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRangeProvider::GetChildren


## -description


Retrieves a collection of all embedded objects that fall within the text range.


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives the address of an array of pointers to the <a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a> 
                interfaces of all child objects that fall within the range. This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Children that overlap with the text range but are not entirely enclosed by it will also be included in the collection. 
        

The method returns a pointer to an empty collection if there are no child objects. 




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

