---
UID: NF:uiautomationcore.IRawElementProviderFragment.GetEmbeddedFragmentRoots
title: IRawElementProviderFragment::GetEmbeddedFragmentRoots
author: windows-sdk-content
description: Retrieves an array of root fragments that are embedded in the Microsoft UI Automation tree rooted at the current element.
old-location: winauto\uiauto_IRawElementProviderFragment_GetEmbeddedFragmentRoots.htm
old-project: WinAuto
ms.assetid: 3e64956d-5ab3-46b6-87db-4b0770c8f89a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetEmbeddedFragmentRoots, GetEmbeddedFragmentRoots method [Windows Accessibility], GetEmbeddedFragmentRoots method [Windows Accessibility],IRawElementProviderFragment interface, IRawElementProviderFragment interface [Windows Accessibility],GetEmbeddedFragmentRoots method, IRawElementProviderFragment.GetEmbeddedFragmentRoots, IRawElementProviderFragment::GetEmbeddedFragmentRoots, uiauto.uiauto_IRawElementProviderFragment_GetEmbeddedFragmentRoots, uiauto_IRawElementProviderFragment_GetEmbeddedFragmentRoots, uiautomationcore/IRawElementProviderFragment::GetEmbeddedFragmentRoots, winauto.uiauto_IRawElementProviderFragment_GetEmbeddedFragmentRoots
ms.prod: windows
ms.technology: windows-sdk
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
 - IRawElementProviderFragment.GetEmbeddedFragmentRoots
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRawElementProviderFragment::GetEmbeddedFragmentRoots


## -description


Retrieves an array of root fragments that are embedded in the Microsoft UI Automation tree rooted at the current element. 


## -parameters




### -param pRetVal [out, retval]

Type: <b>SAFEARRAY**</b>

Receives an array of pointers to the root fragments, or <b>NULL</b> (see Remarks). This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns an array of fragments only if the current element is hosting another automation framework. 
			Most providers return <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>



<b>Reference</b>
 

 

