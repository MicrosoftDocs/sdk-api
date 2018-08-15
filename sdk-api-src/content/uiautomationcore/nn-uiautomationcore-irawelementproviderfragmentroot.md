---
UID: NN:uiautomationcore.IRawElementProviderFragmentRoot
title: IRawElementProviderFragmentRoot
author: windows-sdk-content
description: Exposes methods and properties on the root element in a fragment.
old-location: winauto\uiauto_IRawElementProviderFragmentRoot.htm
old-project: WinAuto
ms.assetid: 16e51962-915e-40ea-a7a1-6f5a5809ba05
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IRawElementProviderFragmentRoot, IRawElementProviderFragmentRoot interface [Windows Accessibility], IRawElementProviderFragmentRoot interface [Windows Accessibility],described, uiauto.uiauto_IRawElementProviderFragmentRoot, uiauto_IRawElementProviderFragmentRoot, uiautomationcore/IRawElementProviderFragmentRoot, winauto.uiauto_IRawElementProviderFragmentRoot
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.redist: 
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
 - UIAutomationCore.dll
api_name:
 - IRawElementProviderFragmentRoot
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IRawElementProviderFragmentRoot interface


## -description


Exposes methods and properties on the root element in a fragment.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderFragmentRoot</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRawElementProviderFragmentRoot</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRawElementProviderFragmentRoot</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/469149c7-8c2c-468c-b7cc-6d849de427f1">ElementProviderFromPoint</a>
</td>
<td align="left" width="63%">
Retrieves the provider of the element that is at the specified point in this fragment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73b5ffc8-1a24-4fa5-8bc4-ae09656a80df">GetFocus</a>
</td>
<td align="left" width="63%">
Retrieves the element in this fragment that has the input focus.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by a root element within a framework; for example, a list box within a window. 
			Other elements in the same fragment, such as list items, implement the <a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>



<a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>



<b>Reference</b>
 

 

