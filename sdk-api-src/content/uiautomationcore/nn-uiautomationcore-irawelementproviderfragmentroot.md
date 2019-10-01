---
UID: NN:uiautomationcore.IRawElementProviderFragmentRoot
title: IRawElementProviderFragmentRoot (uiautomationcore.h)
author: windows-sdk-content
description: Exposes methods and properties on the root element in a fragment.
old-location: winauto\uiauto_IRawElementProviderFragmentRoot.htm
tech.root: WinAuto
ms.assetid: 16e51962-915e-40ea-a7a1-6f5a5809ba05
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRawElementProviderFragmentRoot, IRawElementProviderFragmentRoot interface [Windows Accessibility], IRawElementProviderFragmentRoot interface [Windows Accessibility],described, uiauto.uiauto_IRawElementProviderFragmentRoot, uiauto_IRawElementProviderFragmentRoot, uiautomationcore/IRawElementProviderFragmentRoot, winauto.uiauto_IRawElementProviderFragmentRoot
ms.topic: interface
f1_keywords: 
 - "uiautomationcore/IRawElementProviderFragmentRoot"
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
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IRawElementProviderFragmentRoot
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRawElementProviderFragmentRoot interface


## -description


Exposes methods and properties on the root element in a fragment.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRawElementProviderFragmentRoot</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRawElementProviderFragmentRoot</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragmentroot-elementproviderfrompoint">ElementProviderFromPoint</a>
</td>
<td align="left" width="63%">
Retrieves the provider of the element that is at the specified point in this fragment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragmentroot-getfocus">GetFocus</a>
</td>
<td align="left" width="63%">
Retrieves the element in this fragment that has the input focus.

</td>
</tr>
</table> 


## -remarks



This interface is implemented by a root element within a framework; for example, a list box within a window. 
			Other elements in the same fragment, such as list items, implement the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>



<b>Reference</b>
 

 

